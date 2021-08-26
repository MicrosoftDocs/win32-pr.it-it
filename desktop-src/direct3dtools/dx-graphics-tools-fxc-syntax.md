---
title: Sintassi
description: Ecco la sintassi per chiamare FXC.exe, lo strumento effect-compiler. Per un esempio, vedere Compilazione offline.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- fxc, sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9cae0305a8fdca5c9fd419cf610b0ebbb547331
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880770"
---
# <a name="syntax"></a>Sintassi

Ecco la sintassi per chiamare FXC.exe, lo strumento effect-compiler. Per un esempio, vedere [Compilazione offline.](dx-graphics-tools-fxc-using.md)

-   [Utilizzo](#usage)
-   [Argomenti](#arguments)
-   [Osservazioni:](#remarks)
-   [Profili](#profiles)
-   [Note sulla versione](#version-notes)
-   [Argomenti correlati](#related-topics)

## <a name="usage"></a>Utilizzo

**Fxc** *SwitchOptions* *Filenames*

## <a name="arguments"></a>Argomenti
Separare ogni opzione con uno spazio o due punti.

### <a name="switchoptions"></a>*Opzioni switch*
\[in \] Opzioni di compilazione. È disponibile una sola opzione obbligatoria e molte altre facoltative. Separare ognuno con uno spazio o due punti.

#### <a name="required-option"></a>Opzione obbligatoria
##### <a name="t-profile"></a>/T <*profilo*>
Modello shader (vedere [Profili).](#profiles)

#### <a name="optional-options"></a>Opzioni facoltative
##### <a name="-help"></a>/?, /help
Stampare la Guida per `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*command.option.file*>
File che contiene opzioni di compilazione aggiuntive. Questa opzione può essere mista ad altre opzioni di compilazione della riga di comando. Il *file command.option.file* deve contenere una sola opzione per riga. *Command.option.file non* può contenere righe vuote. Le opzioni specificate nel file non devono contenere spazi iniziali o finali.

##### <a name="all_resources_bound"></a>/all_resources_bound
Abilitare l'appiattimento aggressivo in SM5.1+. Novità di Direct3D 12.

##### <a name="cc"></a>/Cc
Assembly con codifica a colori di output.

##### <a name="compress"></a>/compress
Comprimere il bytecode dello shader DX10 dai file.

##### <a name="d-idtext"></a>/D <*id* >=< *testo*>
Definire la macro.

##### <a name="decompress"></a>/decompress
Decomprimere il bytecode dello shader DX10 dal primo file. I file di output devono essere elencati nell'ordine in cui si trovavano durante la compressione.

##### <a name="dumpbin"></a>/dumpbin
Carica un file binario anziché compilare uno shader.

##### <a name="e-ltnamegt"></a>/E &lt; name&gt;
Punto di ingresso dello shader. Se non viene specificato alcun punto di ingresso, **main** viene considerato il nome della voce dello shader.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Abilita le tabelle dei descrittori non associati. Novità di Direct3D 12.

##### <a name="extractrootsignature-file"></a>/extractrootsignature <*file*>
Estrarre la firma radice dal bytecode dello shader. Novità di Direct3D 12.

##### <a name="fc-file"></a>/Fc <*file*>
File di listato di codice dell'assembly di output.

##### <a name="fd-file"></a>File di </Fd >
Estrarre le informazioni del database del programma shader (PDB) e scrivere nel file specificato. Quando si compila lo shader, usare /Fd per generare un file PDB con informazioni di debug dello shader.

##### <a name="fe-file"></a>File di <*/Fe*>
Genera avvisi ed errori nel file specificato.

##### <a name="fh-file"></a>File di <*/Fh*>
File di intestazione di output contenente il codice oggetto.

##### <a name="fl-file"></a>/Fl <*file*
Restituisce una libreria. Richiede il compilatore D3d \_47.dll o una versione successiva della DLL.

##### <a name="fo-file"></a>File di <*/Fo*>
File oggetto di output. Spesso data l'estensione .fxc , anche se vengono usate altre estensioni, ad esempio &quot; &quot; &quot; .o &quot; , &quot; .obj &quot; o &quot; .dxbc &quot; .

##### <a name="fx-file"></a>File di < /Fx>
File di listato esadecimale e codice assembly di output.

##### <a name="gch"></a>/Gch
Compilare come effetto figlio per i fx_4_x personalizzati.

> [!NOTE]
> Il supporto per i profili effetti legacy è deprecato.

##### <a name="gdp"></a>/Gdp
Disabilitare la modalità di prestazioni dell'effetto.

##### <a name="gec"></a>/Gec
Abilitare la modalità di compatibilità con le versioni precedenti.

##### <a name="ges"></a>/Ges
Abilitare la modalità strict.

##### <a name="getprivate-file"></a>/getprivate <*file*>
Salvare i dati privati dal BLOB dello shader (file binario dello shader compilato) nel file specificato. Estrae i dati privati, incorporati in precedenza da /setprivate, dal BLOB dello shader.

È necessario specificare l'opzione /dumpbin con /getprivate. Ad esempio:

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Evitare costrutti di controllo di flusso.

##### <a name="gfp"></a>/Gfp
Preferisce costrutti di controllo di flusso.

##### <a name="gis"></a>/Gis
Forzare la rigidità IEEE.

##### <a name="gpp"></a>/Gpp
Forzare la precisione parziale.
    
##### <a name="i-include"></a>/I <*includere*>
Percorso di inclusione aggiuntivo.

##### <a name="lx"></a>/Lx
Output di valori letterali esadecimali. Richiede il compilatore D3d \_47.dll o una versione successiva della DLL.

##### <a name="matchuavs"></a>/matchUAVs
Trova la corrispondenza delle allocazioni di slot UAV dello shader modello nello shader corrente. Per altre informazioni, vedere <a href="#remarks">Note.</a>

##### <a name="mergeuavs"></a>/mergeUAVs
Unire allocazioni di slot UAV dello shader modello e dello shader corrente. Per altre informazioni, vedere <a href=""></a> <a href="#remarks">Note.</a>

##### <a name="ni"></a>/Ni
Numeri di istruzioni di output negli elenchi di assembly.

##### <a name="no"></a>/No
Offset del byte dell'istruzione di output negli elenchi di assembly. Quando si produce un assembly, usare /No per annotarlo con l'offset di byte per ogni istruzione.

##### <a name="nologo"></a>/nologo
Non visualizza le informazioni sul copyright.

##### <a name="od"></a>/Od
Disabilita le ottimizzazioni. /Od implica /Gfp, anche se l'output potrebbe non essere identico a /Od /Gfp.

##### <a name="op"></a>/Op
Disabilitare i preshader (deprecati).

##### <a name="o0-o1-o2-o3"></a>/O0 /O1, /O2, /O3
Livelli di ottimizzazione. O1 è l'impostazione predefinita.
- O0: disabilita il riordinamento delle istruzioni. Ciò consente di ridurre il carico dei registri e di velocizzare la simulazione del ciclo.
- O1: disabilita il riordinamento delle istruzioni per ps_3_0 e verso l'alto.
- O2 : uguale a O1. Riservato per utilizzi futuri.
- O3 : uguale a O1. Riservato per utilizzi futuri.

##### <a name="p-file"></a>/P <*file*>
Eseguire la pre-elaborazione in un file (deve essere usato da solo).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Rimuovere i dati di debug dal bytecode shader per i profili 4_0+.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Rimuovere i dati privati dal bytecode shader 4_0+. Rimuove i dati privati (sequenza arbitraria di byte) dal BLOB shader (file binario dello shader compilato) precedentemente incorporato con `/setprivate <file>` l'opzione .

È necessario specificare l'opzione /dumpbin con /Qstrip_priv. Ad esempio:

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Rimuovere i dati di reflection dal bytecode shader per i profili 4_0+.

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Rimuovere la firma radice dal bytecode dello shader. Novità di Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Si supponga che UAV/SRV possano essere alias per cs_5_0+. Richiede il compilatore D3d \_47.dll o una versione successiva della DLL.

##### <a name="setprivate-file"></a>/setprivate <*file*>
Aggiungere dati privati nel file specificato al BLOB dello shader compilato. Incorpora il file specificato, che viene considerato come buffer non elaborato, nel BLOB shader. Usare /setprivate per aggiungere dati privati quando si compila uno shader. In caso contrario, usare l'opzione /dumpbin con /setprivate per caricare un oggetto shader esistente e quindi dopo che l'oggetto è in memoria, per aggiungere il BLOB di dati privato. Ad esempio, usare un singolo comando con /setprivate per aggiungere dati privati a un BLOB shader compilato:

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
In caso contrario, usare due comandi in cui il secondo comando carica un oggetto shader e quindi aggiunge dati privati:

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>/setrootsignature <*file*>
Associa la firma radice al bytecode dello shader. Novità di Direct3D 12.

##### <a name="shtemplate-file"></a>/shtemplate <*file*>
Usare il file shader del modello specificato per unire (/mergeUAVs) e le risorse corrispondenti (/matchUAVs). Per altre informazioni, vedere <a href="#remarks">Note.</a>

##### <a name="vd"></a>/Vd
Disabilitare la convalida.

##### <a name="verifyrootsignature-file"></a>/verifyrootsignature <*file*>
Verificare il bytecode dello shader rispetto alla firma radice. Novità di Direct3D 12.

##### <a name="vi"></a>/Vi
Visualizzare i dettagli sul processo di inclusione.

##### <a name="vn-name"></a>/Vn <*nome*>
Usare name come nome di variabile nel file di intestazione.

##### <a name="wx"></a>/WX
Considerare gli avvisi come errori.

##### <a name="zi"></a>/Zi
Abilita le informazioni di debug.

##### <a name="zpc"></a>/Zpc
Eseguire il pack delle matrici nell'ordine delle colonne principali.

##### <a name="zpr"></a>/Zpr
Eseguire il pack delle matrici in ordine principale di riga.

### <a name="filenames"></a>*Nomi file*

\[in \] I file che contengono gli shader e/o gli effetti.

## <a name="remarks"></a>Commenti

Usare le `/mergeUAVs` opzioni , e per `/matchUAVs` `/shtemplate` allineare gli slot di associazione UAV per una catena di shader.

Si supponga di avere shader A.fx, B.fx e C.fx. Per allineare gli slot di associazione UAV per questa catena di shader, sono necessari due passaggi di compilazione:

**Per allineare gli slot di associazione UAV per una catena di shader**

1.  Usare /mergeUAVs per compilare shader e specificare un BLOB shader compilato in precedenza con /shtemplate. Ad esempio:
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Usare /matchUAVs per compilare gli shader e specificare l'ultimo BLOB shader del primo passaggio con /shtemplate. È possibile eseguire la compilazione in qualsiasi ordine. Ad esempio:
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
Non è necessario ricompilare C.fx nel secondo passaggio.

Dopo aver eseguito i due passaggi di compilazione precedenti, è possibile usare A.o, B.o e C.o come BLOB shader finali con slot UAV allineati.

## <a name="profiles"></a>Profiles

Ogni modello shader è etichettato con un profilo HLSL. Per compilare uno shader in base a un particolare modello shader, scegliere il profilo shader appropriato nella tabella seguente.

<table><thead><tr class="header"><th>Tipo shader</th><th>Profiles</th></tr></thead><tbody><tr class="odd"><td>Shader di calcolo</td><td><dl> cs_4_0<br />
cs_4_1<br />
cs_5_0<br />
cs_5_1<br />
</dl></td></tr><tr class="even"><td>Domain shader</td><td><dl> ds_5_0<br />
ds_5_1<br />
</dl></td></tr><tr class="odd"><td>Geometry shader</td><td><dl> gs_4_0<br />
gs_4_1<br />
gs_5_0<br />
gs_5_1<br />
</dl></td></tr><tr class="even"><td>Collegamento dello shader HLSL </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> Per altre informazioni sul collegamento dello shader, vedere <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> e <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph.</strong></a> <br/></td></tr><tr class="odd"><td>Hull shader</td><td><dl> hs_5_0<br />
hs_5_1<br />
</dl></td></tr><tr class="even"><td>Pixel shader</td><td><dl> ps_2_0<br />
ps_2_a<br />
ps_2_b<br />
ps_2_sw<br />
ps_3_0<br />
ps_3_sw<br />
ps_4_0<br />
ps_4_0_level_9_0<br />
ps_4_0_level_9_1<br />
ps_4_0_level_9_3<br />
ps_4_1<br />
ps_5_0<br />
ps_5_1<br />
</dl></td></tr><tr class="odd"><td>Firma radice</td><td><dl> rootsig_1_0<br />
</dl></td></tr><tr class="even"><td>Shader di trama</td><td><dl> tx_1_0<br />
</dl></td></tr><tr class="odd"><td>Vertex shader</td><td><dl> vs_1_1<br />
vs_2_0<br />
vs_2_a<br />
vs_2_sw<br />
vs_3_0<br />
vs_3_sw<br />
vs_4_0<br />
vs_4_0_level_9_0<br />
vs_4_0_level_9_1<br />
vs_4_0_level_9_3<br />
vs_4_1<br />
vs_5_0<br />
vs_5_1<br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a>Note sulla versione

Per Direct3D 12, vedere Specifica delle firme radice [in HLSL,](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl)Associazione di risorse [in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) e Indicizzazione dinamica [tramite HLSL 5.1.](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1)

In Direct3D 10 usare l'API per ottenere il profilo vertice, geometria e pixel shader più adatto a un determinato dispositivo chiamando queste funzioni: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)e [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).

In Direct3D 9 usare i [**metodi GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) o [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) per recuperare i profili vertice e pixel shader supportati da un dispositivo. La [**struttura D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) restituita da questi metodi indica i profili vertice e pixel shader supportati da un dispositivo nei relativi membri **VertexShaderVersion** e **PixelShaderVersion.**

Per esempi, vedere [Compilazione con il compilatore corrente](dx-graphics-tools-fxc-using.md).

## <a name="related-topics"></a>Argomenti correlati

* [Strumento effect-compiler](fxc.md)
