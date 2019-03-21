---- Minecraft Crash Report ----

WARNING: coremods are present:
  SplashAnimationCoremod (SplashAnimation-0.2.1.jar)
  IELoadingPlugin (ImmersiveEngineering-core-0.12-89.jar)
  Inventory Tweaks Coremod (InventoryTweaks-1.63.jar)
  CorePlugin (SmoothFont-mc1.12.2-1.16.2.jar)
  Do not report to Forge! (If you haven't disabled the FoamFix coremod, try disabling it in the config! Note that this bit of text will still appear.) (foamfix-0.10.3-1.12.2.jar)
  LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
  CoreMod (Aroma1997Core-1.12.2-2.0.0.2.jar)
  SpongeCoremod (spongeforge-1.12.2-2768-7.1.6-RC3616.jar)
  ForgelinPlugin (Forgelin-1.8.2.jar)
  RandomPatches (randompatches-1.12.2-1.15.0.1.jar)
  CTMCorePlugin (CTM-MC1.12.2-0.3.3.22.jar)
Contact their authors BEFORE contacting forge

// Ooh. Shiny.

Time: 3/20/19 9:40 PM
Description: Exception in server tick loop

java.lang.NoClassDefFoundError: net/minecraft/world/chunk/BlockStateContainer
	at net.minecraft.world.chunk.storage.ExtendedBlockStorage.<init>(ExtendedBlockStorage.java:21)
	at net.minecraft.world.chunk.storage.AnvilChunkLoader.func_75823_a(AnvilChunkLoader.java:447)
	at net.minecraft.world.chunk.storage.AnvilChunkLoader.checkedReadChunkFromNBT__Async(AnvilChunkLoader.java:128)
	at net.minecraft.world.chunk.storage.AnvilChunkLoader.loadChunk__Async(AnvilChunkLoader.java:92)
	at net.minecraftforge.common.chunkio.ChunkIOProvider.run(ChunkIOProvider.java:70)
	at net.minecraftforge.common.chunkio.ChunkIOExecutor.syncChunkLoad(ChunkIOExecutor.java:92)
	at net.minecraft.world.gen.ChunkProviderServer.loadChunk(ChunkProviderServer.java:118)
	at net.minecraft.world.gen.ChunkProviderServer.func_186028_c(ChunkProviderServer.java:89)
	at net.minecraft.world.gen.ChunkProviderServer.redirect$onProvideChunkHead$zmm000(ChunkProviderServer.java:678)
	at net.minecraft.world.gen.ChunkProviderServer.func_186025_d(ChunkProviderServer.java:135)
	at net.minecraft.server.MinecraftServer.prepareSpawnArea(MinecraftServer.java:3590)
	at org.spongepowered.common.world.WorldManager.createWorldFromProperties(WorldManager.java:828)
	at org.spongepowered.common.world.WorldManager.loadAllWorlds(WorldManager.java:769)
	at net.minecraft.server.MinecraftServer.func_71247_a(MinecraftServer.java:3541)
	at net.minecraft.server.dedicated.DedicatedServer.func_71197_b(DedicatedServer.java:270)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:486)
	at java.lang.Thread.run(Thread.java:748)
Caused by: java.lang.ClassNotFoundException: net.minecraft.world.chunk.BlockStateContainer
	at net.minecraft.launchwrapper.LaunchClassLoader.findClass(LaunchClassLoader.java:191)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:424)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:357)
	... 17 more
Caused by: org.spongepowered.asm.mixin.transformer.throwables.MixinTransformerError: An unexpected critical error was encountered
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClassBytes(MixinTransformer.java:521)
	at org.spongepowered.asm.mixin.transformer.Proxy.transform(Proxy.java:72)
	at net.minecraft.launchwrapper.LaunchClassLoader.runTransformers(LaunchClassLoader.java:279)
	at net.minecraft.launchwrapper.LaunchClassLoader.findClass(LaunchClassLoader.java:176)
	... 19 more
Caused by: org.spongepowered.asm.mixin.injection.throwables.InjectionError: Critical injection failure: Redirector redirect$onGetStorageSize$FixVanillaBug$zmj000(Lnet/minecraft/util/BitArray;)I in mixins.common.core.json:world.chunk.MixinBlockStateContainer failed injection check, (0/1) succeeded. Using refmap mixins.common.refmap.json
	at org.spongepowered.asm.mixin.injection.struct.InjectionInfo.postInject(InjectionInfo.java:290)
	at org.spongepowered.asm.mixin.transformer.MixinTargetContext.applyInjections(MixinTargetContext.java:1203)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyInjections(MixinApplicatorStandard.java:938)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.applyMixin(MixinApplicatorStandard.java:322)
	at org.spongepowered.asm.mixin.transformer.MixinApplicatorStandard.apply(MixinApplicatorStandard.java:280)
	at org.spongepowered.asm.mixin.transformer.TargetClassContext.applyMixins(TargetClassContext.java:353)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.apply(MixinTransformer.java:724)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.applyMixins(MixinTransformer.java:703)
	at org.spongepowered.asm.mixin.transformer.MixinTransformer.transformClassBytes(MixinTransformer.java:509)
	... 22 more


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Server thread
Stacktrace:
	at net.minecraft.world.chunk.storage.ExtendedBlockStorage.<init>(ExtendedBlockStorage.java:21)
	at net.minecraft.world.chunk.storage.AnvilChunkLoader.func_75823_a(AnvilChunkLoader.java:447)
	at net.minecraft.world.chunk.storage.AnvilChunkLoader.checkedReadChunkFromNBT__Async(AnvilChunkLoader.java:128)
	at net.minecraft.world.chunk.storage.AnvilChunkLoader.loadChunk__Async(AnvilChunkLoader.java:92)
	at net.minecraftforge.common.chunkio.ChunkIOProvider.run(ChunkIOProvider.java:70)
	at net.minecraftforge.common.chunkio.ChunkIOExecutor.syncChunkLoad(ChunkIOExecutor.java:92)
	at net.minecraft.world.gen.ChunkProviderServer.loadChunk(ChunkProviderServer.java:118)
	at net.minecraft.world.gen.ChunkProviderServer.func_186028_c(ChunkProviderServer.java:89)
	at net.minecraft.world.gen.ChunkProviderServer.redirect$onProvideChunkHead$zmm000(ChunkProviderServer.java:678)
	at net.minecraft.world.gen.ChunkProviderServer.func_186025_d(ChunkProviderServer.java:135)
	at net.minecraft.server.MinecraftServer.prepareSpawnArea(MinecraftServer.java:3590)
	at org.spongepowered.common.world.WorldManager.createWorldFromProperties(WorldManager.java:828)

-- Sponge PhaseTracker --
Details:
	Phase Stack: [Empty stack]
Stacktrace:
	at net.minecraft.server.MinecraftServer.handler$onCrashReport$zjn000(MinecraftServer.java:3965)
	at net.minecraft.server.MinecraftServer.func_71230_b(MinecraftServer.java:889)
	at net.minecraft.server.dedicated.DedicatedServer.func_71230_b(DedicatedServer.java:371)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:558)
	at java.lang.Thread.run(Thread.java:748)

-- System Details --
Details:
	Minecraft Version: 1.12.2
	Operating System: Linux (amd64) version 4.4.0-62-generic
	Java Version: 1.8.0_202, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 1255465152 bytes (1197 MB) / 2580021248 bytes (2460 MB) up to 2580021248 bytes (2460 MB)
	JVM Flags: 2 total; -Xmx2560M -Xms2560M
	IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 0
	FML: MCP 9.42 Powered by Forge 14.23.5.2811 140 mods loaded, 140 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored

	| State  | ID                        | Version                  | Source                                          | Signature                                |
	|:------ |:------------------------- |:------------------------ |:----------------------------------------------- |:---------------------------------------- |
	| LCHIJA | minecraft                 | 1.12.2                   | minecraft.jar                                   | None                                     |
	| LCHIJA | mcp                       | 9.42                     | minecraft.jar                                   | None                                     |
	| LCHIJA | FML                       | 8.0.99.99                | FTB_UltimateReloaded_1.4.0.jar                  | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| LCHIJA | forge                     | 14.23.5.2811             | FTB_UltimateReloaded_1.4.0.jar                  | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| LCHIJA | smoothfontcore            | mc1.12.2-1.16            | minecraft.jar                                   | None                                     |
	| LCHIJA | spongeapi                 | 7.1.0-672794fe           | spongeforge-1.12.2-2768-7.1.6-RC3616.jar        | None                                     |
	| LCHIJA | sponge                    | 1.12.2-7.1.6-SNAPSHOT    | spongeforge-1.12.2-2768-7.1.6-RC3616.jar        | None                                     |
	| LCHIJA | spongeforge               | 1.12.2-2768-7.1.6-RC3616 | spongeforge-1.12.2-2768-7.1.6-RC3616.jar        | None                                     |
	| LCHIJA | foamfixcore               | 7.7.4                    | minecraft.jar                                   | None                                     |
	| LCHIJA | randompatches             | 1.12.2-1.15.0.1          | randompatches-1.12.2-1.15.0.1.jar               | None                                     |
	| LCHIJA | ic2                       | 2.8.111-ex112            | industrialcraft-2-2.8.111-ex112.jar             | de041f9f6187debbc77034a344134053277aa3b0 |
	| LCHIJA | advanced_machines         | 61.0.1                   | Advanced Machines-61.0.1.jar                    | None                                     |
	| LCHIJA | advanced_solar_panels     | 4.3.0                    | Advanced Solar Panels-4.3.0.jar                 | None                                     |
	| LCHIJA | appliedenergistics2       | rv6-stable-6             | appliedenergistics2-rv6-stable-6.jar            | dfa4d3ac143316c6f32aa1a1beda1e34d42132e5 |
	| LCHIJA | bdlib                     | 1.14.3.12                | bdlib-1.14.3.12-mc1.12.2.jar                    | None                                     |
	| LCHIJA | ae2stuff                  | 0.7.0.4                  | ae2stuff-0.7.0.4-mc1.12.2.jar                   | None                                     |
	| LCHIJA | charset                   | 0.5.5.6                  | Charset-Lib-0.5.5.6.jar                         | None                                     |
	| LCHIJA | crafttweaker              | 4.1.15                   | CraftTweaker2-1.12-4.1.15.jar                   | None                                     |
	| LCHIJA | mtlib                     | 3.0.6                    | MTLib-3.0.6.jar                                 | None                                     |
	| LCHIJA | modtweaker                | 4.0.16                   | modtweaker-4.0.16.jar                           | None                                     |
	| LCHIJA | jei                       | 4.15.0.268               | jei_1.12.2-4.15.0.268.jar                       | None                                     |
	| LCHIJA | appleskin                 | 1.0.9                    | AppleSkin-mc1.12-1.0.9.jar                      | None                                     |
	| LCHIJA | aroma1997core             | 2.0.0.2                  | Aroma1997Core-1.12.2-2.0.0.2.jar                | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| LCHIJA | aroma1997sdimension       | 2.0.0.2                  | Aroma1997s-Dimensional-World-1.12.2-2.0.0.2.jar | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| LCHIJA | morphtool                 | 1.2-21                   | Morph-o-Tool-1.2-21.jar                         | None                                     |
	| LCHIJA | autoreglib                | 1.3-26                   | AutoRegLib-1.3-26.jar                           | None                                     |
	| LCHIJA | baubles                   | 1.5.2                    | Baubles-1.12-1.5.2.jar                          | None                                     |
	| LCHIJA | bibliocraft               | 2.4.5                    | BiblioCraft[v2.4.5][MC1.12.2].jar               | None                                     |
	| LCHIJA | buildcraftlib             | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | buildcraftcore            | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | buildcraftenergy          | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | reborncore                | 3.13.6.424               | RebornCore-1.12.2-3.13.6.424-universal.jar      | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
	| LCHIJA | techreborn                | 2.21.1.954               | TechReborn-1.12.2-2.21.1.954-universal.jar      | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
	| LCHIJA | forestry                  | 5.8.2.387                | forestry_1.12.2-5.8.2.387.jar                   | None                                     |
	| LCHIJA | binniecore                | 2.5.1.188                | binnie-mods-1.12.2-2.5.1.188.jar                | None                                     |
	| LCHIJA | binniedesign              | 2.5.1.188                | binnie-mods-1.12.2-2.5.1.188.jar                | None                                     |
	| LCHIJA | genetics                  | 2.5.1.188                | binnie-mods-1.12.2-2.5.1.188.jar                | None                                     |
	| LCHIJA | botany                    | 2.5.1.188                | binnie-mods-1.12.2-2.5.1.188.jar                | None                                     |
	| LCHIJA | extrabees                 | 2.5.1.188                | binnie-mods-1.12.2-2.5.1.188.jar                | None                                     |
	| LCHIJA | extratrees                | 2.5.1.188                | binnie-mods-1.12.2-2.5.1.188.jar                | None                                     |
	| LCHIJA | blockcraftery             | 1.12.2-1.2.0             | blockcraftery-1.12.2-1.2.0.jar                  | None                                     |
	| LCHIJA | buildcraftbuilders        | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | buildcrafttransport       | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | buildcraftsilicon         | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | theoneprobe               | 1.4.28                   | theoneprobe-1.12-1.4.28.jar                     | None                                     |
	| LCHIJA | buildcraftcompat          | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | buildcraftfactory         | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | buildcraftrobotics        | 7.99.22                  | buildcraft-all-7.99.22.jar                      | None                                     |
	| LCHIJA | computercraft             | 1.81.1                   | cc-tweaked-1.12.2-1.81.1.jar                    | None                                     |
	| LCHIJA | chisel                    | MC1.12.2-0.2.1.35        | Chisel-MC1.12.2-0.2.1.35.jar                    | None                                     |
	| LCHIJA | chiselsandbits            | 14.30                    | chiselsandbits-14.30.jar                        | None                                     |
	| LCHIJA | codechickenlib            | 3.2.2.353                | CodeChickenLib-1.12.2-3.2.2.353-universal.jar   | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| LCHIJA | redstoneflux              | 2.1.0                    | RedstoneFlux-1.12-2.1.0.6-universal.jar         | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| LCHIJA | cofhcore                  | 4.6.2                    | CoFHCore-1.12.2-4.6.2.25-universal.jar          | None                                     |
	| LCHIJA | cofhworld                 | 1.3.0                    | CoFHWorld-1.12.2-1.3.0.6-universal.jar          | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| LCHIJA | compactsolars             | 1.12.2-5.0.18.341        | CompactSolars-1.12.2-5.0.18.341-universal.jar   | None                                     |
	| LCHIJA | asielib                   | 1.0.0                    | Computronics-1.12.2-1.6.6.192-rc-beta-5.jar     | None                                     |
	| LCHIJA | thaumcraft                | 6.1.BETA26               | Thaumcraft-1.12.2-6.1.BETA26.jar                | None                                     |
	| LCHIJA | railcraft                 | 12.0.0-beta-5            | railcraft-12.0.0-beta-5.jar                     | a0c255ac501b2749537d5824bb0f0588bf0320fa |
	| LCHIJA | computronics              | 1.6.6                    | Computronics-1.12.2-1.6.6.192-rc-beta-5.jar     | None                                     |
	| LCHIJA | craftingtweaks            | 8.1.9                    | CraftingTweaks_1.12.2-8.1.9.jar                 | None                                     |
	| LCHIJA | crafttweakerjei           | 2.0.2                    | CraftTweaker2-1.12-4.1.15.jar                   | None                                     |
	| LCHIJA | diethopper                | 1.1                      | diethopper-1.1.jar                              | None                                     |
	| LCHIJA | enderstorage              | 2.4.5.135                | EnderStorage-1.12.2-2.4.5.135-universal.jar     | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| LCHIJA | energyconverters          | 1.2.1.11                 | energyconverters_1.12.2-1.2.1.11.jar            | None                                     |
	| LCHIJA | ffs                       | 1.12.2-2.2.3             | Fancy_Fluid_Storage-1.12.2-2.2.3.jar            | None                                     |
	| LCHIJA | fastbench                 | 1.6.1                    | FastWorkbench-1.12.2-1.6.1.jar                  | None                                     |
	| LCHIJA | flatcoloredblocks         | mc1.12-6.6               | flatcoloredblocks-mc1.12-6.6.jar                | None                                     |
	| LCHIJA | foamfix                   | 0.10.3-1.12.2            | foamfix-0.10.3-1.12.2.jar                       | None                                     |
	| LCHIJA | forgelin                  | 1.8.2                    | Forgelin-1.8.2.jar                              | None                                     |
	| LCHIJA | forgemultipartcbe         | 2.6.1.81                 | ForgeMultipart-1.12.2-2.6.1.81-universal.jar    | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| LCHIJA | microblockcbe             | 2.6.1.81                 | ForgeMultipart-1.12.2-2.6.1.81-universal.jar    | None                                     |
	| LCHIJA | minecraftmultipartcbe     | 2.6.1.81                 | ForgeMultipart-1.12.2-2.6.1.81-universal.jar    | None                                     |
	| LCHIJA | ftblib                    | 5.4.1.88                 | FTBLib-5.4.1.88.jar                             | None                                     |
	| LCHIJA | ftbutilities              | 5.4.0.85                 | FTBUtilities-5.4.0.85.jar                       | None                                     |
	| LCHIJA | ftbbackups                | 0.0.0.ftbbackups         | FTBUtilitiesBackups-1.0.0.2.jar                 | None                                     |
	| LCHIJA | gravisuite                | 3.1.0                    | Gravitation Suite-3.1.0.jar                     | None                                     |
	| LCHIJA | ichunutil                 | 7.2.1                    | iChunUtil-1.12.2-7.2.1.jar                      | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
	| LCHIJA | gravitygun                | 7.0.0                    | GravityGun-1.12.2-7.0.1.jar                     | None                                     |
	| LCHIJA | modularrouters            | 1.12.2-3.2.1             | modular-routers-1.12.2-3.2.1.jar                | None                                     |
	| LCHIJA | guideapi                  | 1.12-2.1.8-63            | Guide-API-1.12-2.1.8-63.jar                     | None                                     |
	| LCHIJA | harvest                   | 1.12-1.2.7-20            | Harvest-1.12-1.2.7-20.jar                       | None                                     |
	| LCHIJA | thermalfoundation         | 2.6.2                    | ThermalFoundation-1.12.2-2.6.2.26-universal.jar | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| LCHIJA | twilightforest            | 3.8.689                  | twilightforest-1.12.2-3.8.689-universal.jar     | None                                     |
	| LCHIJA | immersiveengineering      | 0.12-89                  | ImmersiveEngineering-0.12-89.jar                | 4cb49fcde3b43048c9889e0a3d083225da926334 |
	| LCHIJA | immersivecables           | 1.3.2                    | ImmersiveCables-1.12.2-1.3.2.jar                | None                                     |
	| LCHIJA | teslacorelib              | 1.0.15                   | tesla-core-lib-1.12.2-1.0.15.jar                | d476d1b22b218a10d845928d1665d45fce301b27 |
	| LCHIJA | industrialforegoing       | 1.12.2-1.12.2            | industrialforegoing-1.12.2-1.12.7-231.jar       | None                                     |
	| LCHIJA | simplecorn                | 2.4.1                    | SimpleCorn1.12-1.12-2.4.1.jar                   | None                                     |
	| LCHIJA | integrationforegoing      | 1.12.2-1.9               | IntegrationForegoing-1.12.2-1.9.jar             | 4ffa87db52cf086d00ecc4853a929367b1c39b5c |
	| LCHIJA | inventorytweaks           | 1.63+release.109.220f184 | InventoryTweaks-1.63.jar                        | 55d2cd4f5f0961410bf7b91ef6c6bf00a766dcbe |
	| LCHIJA | ironchest                 | 1.12.2-7.0.59.842        | ironchest-1.12.2-7.0.59.842.jar                 | None                                     |
	| LCHIJA | jeibees                   | 0.9.0.5                  | jeibees-0.9.0.5-mc1.12.2.jar                    | None                                     |
	| LCHIJA | jee                       | 1.0.6                    | JustEnoughEnergistics-1.12.2-1.0.6.jar          | None                                     |
	| LCHIJA | longfallboots             | 1.2.1a                   | longfallboots-1.2.1b.jar                        | None                                     |
	| LCHIJA | magicbees                 | 1.0                      | MagicBees-1.12.2-3.1.10.jar                     | None                                     |
	| LCHIJA | mcmultipart               | 2.5.3                    | MCMultiPart-2.5.3.jar                           | None                                     |
	| LCHIJA | modularforcefieldsystem   | 3.0.1                    | MFFS-1.12.2-4.0.1.0_1.12_cc3a5aa.jar            | None                                     |
	| LCHIJA | minetogether              | unspecified              | minetogether-1.10.2-2.1.3.jar                   | None                                     |
	| LCHIJA | minetogetherserver        | unspecified              | minetogether-1.10.2-2.1.3.jar                   | None                                     |
	| LCHIJA | numina                    | 1.10.0                   | ModularPowersuits-1.12.2-0.7.0.035.jar          | None                                     |
	| LCHIJA | powersuits                | 1.12.2-0.7.0.035         | ModularPowersuits-1.12.2-0.7.0.035.jar          | None                                     |
	| LCHIJA | morpheus                  | 1.12.2-3.5.106           | Morpheus-1.12.2-3.5.106.jar                     | None                                     |
	| LCHIJA | mrtjpcore                 | 2.1.3.35                 | MrTJPCore-1.12.2-2.1.3.35-universal.jar         | None                                     |
	| LCHIJA | netherendingores          | 1.12.2-1.3               | Netherending-Ores-1.12.2-1.3.jar                | None                                     |
	| LCHIJA | placebo                   | 1.5.1                    | Placebo-1.12.2-1.5.1.jar                        | None                                     |
	| LCHIJA | playerplates              | 1.12.2-1.3.1.1           | playerplates-1.12.2-1.3.1.1.jar                 | None                                     |
	| LCHIJA | portalgun                 | 7.1.0                    | PortalGun-1.12.2-7.1.0.jar                      | 4db5c2bd1b556f252a5b8b54b256d381b2a0a6b8 |
	| LCHIJA | projectred-core           | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-Base.jar             | None                                     |
	| LCHIJA | projectred-compat         | 1.0                      | ProjectRed-1.12.2-4.9.1.92-compat.jar           | None                                     |
	| LCHIJA | projectred-integration    | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-integration.jar      | None                                     |
	| LCHIJA | projectred-transmission   | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-integration.jar      | None                                     |
	| LCHIJA | projectred-fabrication    | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-fabrication.jar      | None                                     |
	| LCHIJA | projectred-illumination   | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-lighting.jar         | None                                     |
	| LCHIJA | projectred-expansion      | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-mechanical.jar       | None                                     |
	| LCHIJA | projectred-relocation     | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-mechanical.jar       | None                                     |
	| LCHIJA | projectred-transportation | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-mechanical.jar       | None                                     |
	| LCHIJA | projectred-exploration    | 4.9.1.92                 | ProjectRed-1.12.2-4.9.1.92-world.jar            | None                                     |
	| LCHIJA | projectx                  | 2.2.7                    | ProjectX-1.12.2-2.2.7-universal.jar             | None                                     |
	| LCHIJA | xreliquary                | 1.12.2-1.3.4.786         | Reliquary-1.12.2-1.3.4.786.jar                  | None                                     |
	| LCHIJA | retroexchange             | 1.0.0                    | Retro-Exchange-1.12.2-1.0.7.jar                 | None                                     |
	| LCHIJA | silverfish                | 0.0.19                   | Silverfish-1.12.2-0.0.19-universal.jar          | None                                     |
	| LCHIJA | soulshardsrespawn         | 1.12.2-1.1.0-12          | SoulShardsRespawn-1.12.2-1.1.0-12.jar           | None                                     |
	| LCHIJA | stevescarts               | 2.4.29.132               | StevesCarts-1.12.2-2.4.29.132.jar               | None                                     |
	| LCHIJA | thaumicenergistics        | 2.2.1                    | thaumicenergistics-2.2.1.jar                    | None                                     |
	| LCHIJA | tcinventoryscan           | 2.0.10                   | ThaumicInventoryScanning_1.12.2-2.0.10.jar      | None                                     |
	| LCHIJA | thaumictinkerer           | 1.12.2-5.0-353c71c       | thaumictinkerer-1.12.2-5.0-353c71c.jar          | None                                     |
	| LCHIJA | thermalexpansion          | 5.5.3                    | ThermalExpansion-1.12.2-5.5.3.41-universal.jar  | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| LCHIJA | thermaldynamics           | 2.5.4                    | ThermalDynamics-1.12.2-2.5.4.18-universal.jar   | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| LCHIJA | topaddons                 | 1.12.2-1.10.1            | topaddons-1.12.2-1.10.1.jar                     | None                                     |
	| LCHIJA | torchmaster               | 1.7.1.74                 | torchmaster_1.12.2-1.7.1.74.jar                 | 5e9a436b366831c8f54a7e80b015784da69278c6 |
	| LCHIJA | traverse                  | 1.6.0                    | Traverse-1.12.2-1.6.0-69.jar                    | None                                     |
	| LCHIJA | wanionlib                 | 1.12.2-2.2               | WanionLib-1.12.2-2.2.jar                        | None                                     |
	| LCHIJA | worldcontrol              | 1.0.18                   | WorldControl-1.0.18.jar                         | None                                     |
	| LCHIJA | wrcbe                     | 2.3.1                    | WR-CBE-1.12.2-2.3.1.30-universal.jar            | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| LCHIJA | yabba                     | 1.1.2.45                 | YABBA-1.1.2.45.jar                              | None                                     |
	| LCHIJA | techreborn_compat         | 1.0.0                    | TechReborn-ModCompatibility-1.12.2-1.1.0.36.jar | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
	| LCHIJA | mysticallib               | 1.12.2-1.1.1             | mysticallib-1.12.2-1.1.1.jar                    | None                                     |
	| LCHIJA | teslacorelib_registries   | 1.0.15                   | tesla-core-lib-1.12.2-1.0.15.jar                | None                                     |
	| LCHIJA | unidict                   | 1.12.2-2.9.2             | UniDict-1.12.2-2.9.2.jar                        | None                                     |

	Loaded coremods (and transformers): 
SplashAnimationCoremod (SplashAnimation-0.2.1.jar)
  pl.asie.splashanimation.core.SplashProgressTransformer
IELoadingPlugin (ImmersiveEngineering-core-0.12-89.jar)
  blusunrize.immersiveengineering.common.asm.IEClassTransformer
Inventory Tweaks Coremod (InventoryTweaks-1.63.jar)
  invtweaks.forge.asm.ContainerTransformer
CorePlugin (SmoothFont-mc1.12.2-1.16.2.jar)
  bre.smoothfont.asm.Transformer
Do not report to Forge! (If you haven't disabled the FoamFix coremod, try disabling it in the config! Note that this bit of text will still appear.) (foamfix-0.10.3-1.12.2.jar)
  pl.asie.foamfix.coremod.FoamFixTransformer
LoadingPlugin (ResourceLoader-MC1.12.1-1.5.3.jar)
  lumien.resourceloader.asm.ClassTransformer
CoreMod (Aroma1997Core-1.12.2-2.0.0.2.jar)
  
SpongeCoremod (spongeforge-1.12.2-2768-7.1.6-RC3616.jar)
  org.spongepowered.common.launch.transformer.SpongeSuperclassTransformer
ForgelinPlugin (Forgelin-1.8.2.jar)
  
RandomPatches (randompatches-1.12.2-1.15.0.1.jar)
  com.therandomlabs.randompatches.core.RPTransformer
CTMCorePlugin (CTM-MC1.12.2-0.3.3.22.jar)
  team.chisel.ctm.client.asm.CTMTransformer
	AE2 Version: stable rv6-stable-6 for Forge 14.23.5.2768
	List of loaded APIs: 
		* appliedenergistics2|API (rv6) from appliedenergistics2-rv6-stable-6.jar
		* asielibAPI (1.1) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* asielibAPI|tile (1.0) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* asielibAPI|tool (1.1) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* Baubles|API (1.4.0.2) from Baubles-1.12-1.5.2.jar
		* betteradvancements|API (0.1.0.77) from BetterAdvancements-1.12.2-0.1.0.77.jar
		* BetterWithModsAPI (Beta 0.6) from AppleSkin-mc1.12-1.0.9.jar
		* buildcraftapi_blocks (1.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_boards (2.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_core (2.2) from buildcraft-all-7.99.22.jar
		* buildcraftapi_crops (1.1) from buildcraft-all-7.99.22.jar
		* buildcraftapi_enums (1.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_events (2.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_facades (1.1) from buildcraft-all-7.99.22.jar
		* buildcraftapi_filler (5.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_fuels (2.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_gates (4.1) from buildcraft-all-7.99.22.jar
		* buildcraftapi_items (1.1) from buildcraft-all-7.99.22.jar
		* buildcraftapi_library (2.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_lists (1.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_power (1.3) from buildcraft-all-7.99.22.jar
		* buildcraftapi_recipes (3.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_robotics (3.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_statements (1.1) from buildcraft-all-7.99.22.jar
		* buildcraftapi_tiles (1.2) from buildcraft-all-7.99.22.jar
		* buildcraftapi_tools (1.0) from buildcraft-all-7.99.22.jar
		* buildcraftapi_transport (5.0) from buildcraft-all-7.99.22.jar
		* CharsetAPI (0.1) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Audio (0.0) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Carry (0.0) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Laser (0.0) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Lib (0.2) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Locks (0.1) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Pipes (0.3) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Storage (0.1) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Tape (0.0) from Charset-Lib-0.5.5.6.jar
		* CharsetAPI|Wires (0.3) from Charset-Lib-0.5.5.6.jar
		* Chisel-API (0.0.1) from Chisel-MC1.12.2-0.2.1.35.jar
		* ChiselAPI|Carving (0.0.1) from Chisel-MC1.12.2-0.2.1.35.jar
		* ChiselsAndBitsAPI (14.25.0) from chiselsandbits-14.30.jar
		* cofhapi (2.5.0) from CoFHCore-1.12.2-4.6.2.25-universal.jar
		* ComputerCraft|API (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|FileSystem (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Lua (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Media (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Network (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Network|Wired (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Peripheral (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Permissions (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Redstone (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Turtle (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* ComputerCraft|API|Turtle|Event (1.81.1) from cc-tweaked-1.12.2-1.81.1.jar
		* computronicsAPI (1.3) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* computronicsAPI|audio (1.0) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* computronicsAPI|chat (1.3) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* computronicsAPI|multiperipheral (1.1) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* computronicsAPI|tape (1.0) from Computronics-1.12.2-1.6.6.192-rc-beta-5.jar
		* CraftingTweaks|API (4.1) from CraftingTweaks_1.12.2-8.1.9.jar
		* ctm-api (0.1.0) from CTM-MC1.12.2-0.3.3.22.jar
		* ctm-api-events (0.1.0) from CTM-MC1.12.2-0.3.3.22.jar
		* ctm-api-models (0.1.0) from CTM-MC1.12.2-0.3.3.22.jar
		* ctm-api-textures (0.1.0) from CTM-MC1.12.2-0.3.3.22.jar
		* ctm-api-utils (0.1.0) from CTM-MC1.12.2-0.3.3.22.jar
		* ForestryAPI|apiculture (5.0.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|arboriculture (4.3.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|book (5.8.1) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|circuits (3.1.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|climate (5.0.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|core (5.7.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|farming (5.8.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|food (1.1.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|fuels (3.0.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|genetics (5.7.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|gui (5.8.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|hives (4.1.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|lepidopterology (1.4.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|mail (3.1.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|modules (5.7.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|multiblock (3.0.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|recipes (5.4.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|storage (5.0.0) from forestry_1.12.2-5.8.2.387.jar
		* ForestryAPI|world (2.1.0) from forestry_1.12.2-5.8.2.387.jar
		* Guide-API|API (2.0.0) from Guide-API-1.12-2.1.8-63.jar
		* iChunUtil API (1.2.0) from iChunUtil-1.12.2-7.2.1.jar
		* ImmersiveEngineering|API (1.0) from ImmersiveEngineering-0.12-89.jar
		* ImmersiveEngineering|ImmersiveFluxAPI (1.0) from ImmersiveEngineering-0.12-89.jar
		* industrialforegoingapi (5) from industrialforegoing-1.12.2-1.12.7-231.jar
		* JustEnoughItemsAPI (4.13.0) from jei_1.12.2-4.15.0.268.jar
		* modtogether|api (1.0) from minetogether-1.10.2-2.1.3.jar
		* MouseTweaks|API (1.0) from MouseTweaks-2.10-mc1.12.2.jar
		* projectred|api (2.0) from ProjectRed-1.12.2-4.9.1.92-Base.jar
		* projectx-api (0.0.1) from ProjectX-1.12.2-2.2.7-universal.jar
		* railcraft:api_carts (3.0.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_charge (4.0.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_core (3.2.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_crafting (4.0.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_events (2.0.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_fuel (2.0.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_helpers (2.0.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_items (2.4.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_signals (4.0.0) from railcraft-12.0.0-beta-5.jar
		* railcraft:api_tracks (5.1.1) from railcraft-12.0.0-beta-5.jar
		* reborncoreAPI (3.13.6.424) from RebornCore-1.12.2-3.13.6.424-universal.jar
		* reborncoreAPI|Power (3.13.6.424) from RebornCore-1.12.2-3.13.6.424-universal.jar
		* reborncoreAPI|Recipe (3.13.6.424) from RebornCore-1.12.2-3.13.6.424-universal.jar
		* reborncoreAPI|Tile (3.13.6.424) from RebornCore-1.12.2-3.13.6.424-universal.jar
		* redstonefluxapi (2.1.0) from RedstoneFlux-1.12-2.1.0.6-universal.jar
		* stevescartsAPI (${version}) from StevesCarts-1.12.2-2.4.29.132.jar
		* stevescartsAPI|FARMS (${version}) from StevesCarts-1.12.2-2.4.29.132.jar
		* techrebornAPI (2.21.1.954) from TechReborn-1.12.2-2.21.1.954-universal.jar
		* Thaumcraft|API (6.0.2) from Thaumcraft-1.12.2-6.1.BETA26.jar
		* theoneprobe_api (1.4.4) from theoneprobe-1.12-1.4.28.jar
	RebornCore: 
		Plugin Engine: 1
		RebornCore Version: 3.13.6.424
		Runtime Debofucsation 1
	forestry : Modules have been disabled in the config: Lepidopterology
	AE2 Integration: IC2:ON, RC:ON, MFR:OFF, Waila:OFF, Mekanism:OFF, OpenComputers:OFF, THE_ONE_PROBE:ON, TESLA:OFF, CRAFTTWEAKER:ON
	Profiler Position: N/A (disabled)
	Player Count: 0 / 50; []
	Is Modded: Definitely; Server brand changed to 'fml,forge,sponge'
	Type: Dedicated Server (map_server.txt)
