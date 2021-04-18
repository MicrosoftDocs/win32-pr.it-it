---
title: Sintassi
description: Di seguito è illustrata la sintassi per chiamare FXC.exe, lo strumento compilatore di effetti. Per un esempio, vedere Compilazione offline.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300600"
---
# <a name="syntax"></a>Sintassi

Di seguito è illustrata la sintassi per chiamare FXC.exe, lo strumento compilatore di effetti. Per un esempio, vedere [compilazione offline](dx-graphics-tools-fxc-using.md).

-   [Utilizzo](#usage)
-   [Argomenti](#arguments)
-   [Osservazioni:](#remarks)
-   [Profili](#profiles)
-   [Note sulla versione](#version-notes)
-   [Argomenti correlati](#related-topics)

## <a name="usage"></a>Utilizzo

*nomi file* *SwitchOptions* **FXC**

## <a name="arguments"></a>Argomenti
Separare ogni opzione con uno spazio o un segno di due punti.

### <a name="switchoptions"></a>*SwitchOptions*
\[in \] Opzioni di compilazione. È disponibile solo un'opzione obbligatoria e molte altre sono facoltative. Separare ognuno con uno spazio o due punti.

#### <a name="required-option"></a>Opzione obbligatoria
##### <a name="t-profile"></a>/T <*profilo*>
Modello shader (vedere [profili](#profiles)).

#### <a name="optional-options"></a>Opzioni facoltative
##### <a name="-help"></a>/?, /help
Stampa la guida per `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*Command. Option. file*>
File che contiene altre opzioni di compilazione. Questa opzione può essere combinata con altre opzioni di compilazione della riga di comando. Il *comando. Option. file* deve contenere solo un'opzione per riga. Il *comando. Option. file* non può contenere righe vuote. Le opzioni specificate nel file non devono contenere spazi iniziali o finali.

##### <a name="all_resources_bound"></a>/all_resources_bound
Abilitare la flatità aggressiva in SM 5.1 +. Novità per Direct3D 12.

##### <a name="cc"></a>/CC
Colore di output: assembly codificato.

##### <a name="compress"></a>/Compress
Comprime il bytecode dello shader DX10 dai file.

##### <a name="d-idtext"></a>/D < >=< *testo* ID>
Definire la macro.

##### <a name="decompress"></a>/decompress
Decomprimere il bytecode dello shader DX10 dal primo file. I file di output devono essere elencati nell'ordine in cui si trovavano durante la compressione.

##### <a name="dumpbin"></a>/dumpbin
Carica un file binario anziché compilare uno shader.

##### <a name="e-name"></a>/E <name>
Punto di ingresso dello shader. Se non viene specificato alcun punto di ingresso, **Main** viene considerato il nome della voce dello shader.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Abilita le tabelle dei descrittori non vincolate. Novità per Direct3D 12.

##### <a name="extractrootsignature-file"></a>*file* </extractrootsignature>
Estrae la firma radice dal bytecode dello shader. Novità per Direct3D 12.

##### <a name="fc-file"></a>*File* </FC>
File di listato di codice dell'assembly di output.

##### <a name="fd-file"></a>*File* </FD>
Estrae le informazioni del database di programma shader (PDB) e scrive nel file specificato. Quando si compila lo shader, usare/FD per generare un file PDB con le informazioni di debug dello shader.

##### <a name="fe-file"></a>*File* </Fe>
Genera avvisi ed errori nel file specificato.

##### <a name="fh-file"></a>*File* </FH>
File di intestazione di output contenente il codice oggetto.

##### <a name="fl-file"></a>*File* </FL
Output di una libreria. Richiede la \_47.dll D3dcompiler o una versione successiva della dll.

##### <a name="fo-file"></a>*File* </fo>
File oggetto di output. Spesso è stata assegnata l'estensione &quot; . fxc &quot; , anche se vengono usate altre estensioni, ad esempio &quot; . o &quot; , &quot; . obj &quot; o &quot; . dxbc &quot; .

##### <a name="fx-file"></a>*File* </FX>
Codice dell'assembly di output e file di elenco esadecimale.

##### <a name="gch"></a>/Gch
Compilare come effetto figlio per i profili di fx_4_x.

> [!NOTE]
> Il supporto per i profili degli effetti legacy è deprecato.

##### <a name="gdp"></a>/Gdp
Disabilitare la modalità prestazioni effetto.

##### <a name="gec"></a>/Gec
Abilitare la modalità di compatibilità con le versioni precedenti.

##### <a name="ges"></a>/Ges
Abilitare la modalità Strict.

##### <a name="getprivate-file"></a>*file* </getprivate>
Salvare i dati privati dal BLOB dello shader (Binary shader compilato) al file specificato. Estrae i dati privati, incorporati in precedenza da/SetPrivate, dal BLOB dello shader.

È necessario specificare l'opzione/DUMPBIN con/getprivate. Ad esempio:

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Evitare costrutti di controllo di flusso.

##### <a name="gfp"></a>/GFP
Preferisce i costrutti di controllo di flusso.

##### <a name="gis"></a>/Gis
Forza la rigidità IEEE.

##### <a name="gpp"></a>/Gpp
Forza la precisione parziale.
    
##### <a name="i-include"></a>/I <*includere*>
Percorso di inclusione aggiuntivo.

##### <a name="lx"></a>/Lx
Output valori letterali esadecimali. Richiede la \_47.dll D3dcompiler o una versione successiva della dll.

##### <a name="matchuavs"></a>/matchUAVs
Corrisponde alle allocazioni degli slot UAV del modello shader nello shader corrente. Per ulteriori informazioni, vedere la <a href="#remarks">sezione Osservazioni</a>.

##### <a name="mergeuavs"></a>/mergeUAVs
Unire le allocazioni degli slot UAV del modello shader e dello shader corrente. Per ulteriori informazioni, vedere la <a href=""></a> <a href="#remarks">sezione Osservazioni</a>.

##### <a name="ni"></a>/Ni
Numeri di istruzioni di output negli elenchi di assembly.

##### <a name="no"></a>/No
Offset di byte dell'istruzione di output negli elenchi di assembly. Quando si genera un assembly, usare/No per annotarlo con l'offset dei byte per ogni istruzione.

##### <a name="nologo"></a>/nologo
Non visualizza le informazioni sul copyright.

##### <a name="od"></a>/Od
Disabilita le ottimizzazioni. /Od implica/GFP, anche se l'output potrebbe non essere identico a/od/GFP.

##### <a name="op"></a>/Op
Disabilitare i preshader (deprecato).

##### <a name="o0-o1-o2-o3"></a>/O0/O1,/O2,/O3
Livelli di ottimizzazione. O1 è l'impostazione predefinita.
- O0-Disabilita il riordinamento delle istruzioni. In questo modo è possibile ridurre il carico del registro e velocizzare la simulazione del ciclo.
- O1: Disabilita il riordinamento delle istruzioni per ps_3_0 e su.
- O2: uguale a o1. Riservato per utilizzi futuri.
- O3: uguale a o1. Riservato per utilizzi futuri.

##### <a name="p-file"></a>/P <*file*>
Pre-elabora nel file (deve essere usato da solo).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Rimuove i dati di debug dal bytecode dello shader per 4_0 + profili.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Rimuovere i dati privati da 4_0 + bytecode shader. Rimuove i dati privati (sequenza arbitraria di byte) dal BLOB dello shader (Binary shader compilato) precedentemente incorporato con l' `/setprivate <file>` opzione.

È necessario specificare l'opzione/DUMPBIN con/Qstrip_priv. Ad esempio:

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Rimuove i dati di reflection dal bytecode dello shader per 4_0 + profili.

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Rimuovere la firma radice dal bytecode dello shader. Novità per Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Si supponga che UAV/SRVs possa essere alias per cs_5_0 +. Richiede la \_47.dll D3dcompiler o una versione successiva della dll.

##### <a name="setprivate-file"></a>*file* </SetPrivate>
Aggiungere i dati privati nel file specificato al BLOB dello shader compilato. Incorpora il file specificato, che viene considerato come un buffer non elaborato, nel BLOB dello shader. Usare/SetPrivate per aggiungere dati privati quando si compila uno shader. In alternativa, usare l'opzione/DUMPBIN con/SetPrivate per caricare un oggetto shader esistente e quindi, dopo che l'oggetto è in memoria, per aggiungere il BLOB di dati privati. Ad esempio, usare un singolo comando con/SetPrivate per aggiungere dati privati a un BLOB dello shader compilato:

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
In alternativa, usare due comandi dove il secondo comando carica un oggetto shader e quindi aggiunge dati privati:

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>*file* </setrootsignature>
Associa la firma radice al bytecode dello shader. Novità per Direct3D 12.

##### <a name="shtemplate-file"></a>*file* </shtemplate>
Usare il file shader del modello specificato per unire (/mergeUAVs) e le risorse corrispondenti (/matchUAVs). Per ulteriori informazioni, vedere la <a href="#remarks">sezione Osservazioni</a>.

##### <a name="vd"></a>/VD
Disabilitare la convalida.

##### <a name="verifyrootsignature-file"></a>*file* </verifyrootsignature>
Verificare il bytecode dello shader rispetto alla firma radice. Novità per Direct3D 12.

##### <a name="vi"></a>/Vi
Visualizza i dettagli sul processo di inclusione.

##### <a name="vn-name"></a>*Nome* </VN>
Usare nome come nome della variabile nel file di intestazione.

##### <a name="wx"></a>/WX
Considera gli avvisi come errori.

##### <a name="zi"></a>/Zi
Abilita le informazioni di debug.

##### <a name="zpc"></a>/Zpc
Comprimere le matrici in base all'ordine delle colonne.

##### <a name="zpr"></a>/Zpr
Comprimere le matrici in ordine di riga.

### <a name="filenames"></a>*Nomi file*

\[nei \] file che contengono gli shader e/o l'effetto o i.

## <a name="remarks"></a>Commenti

Usare le `/mergeUAVs` `/matchUAVs` Opzioni, e `/shtemplate` per allineare gli slot di binding UAV per una catena di shader.

Si supponga di avere shader A. FX, B. FX e C. fx. Per allineare gli slot di binding UAV per questa catena di shader, sono necessari due passaggi di compilazione:

**Per allineare gli slot di binding UAV per una catena di shader**

1.  Usare/mergeUAVs per compilare shader e specificare un BLOB dello shader compilato in precedenza con/shtemplate. Ad esempio:
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Usare/matchUAVs per compilare shader e specificare l'ultimo BLOB dello shader dal primo passaggio con/shtemplate. È possibile compilare in qualsiasi ordine. Ad esempio:
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
Non è necessario ricompilare C. fx nel secondo passaggio.

Dopo aver eseguito le due passate di compilazione precedenti, è possibile usare un. o, B. o e C. o come BLOB dello shader finale con slot UAV allineati.

## <a name="profiles"></a>Profiles

Ogni modello shader è contrassegnato con un profilo HLSL. Per compilare uno shader rispetto a un particolare modello shader, scegliere il profilo shader appropriato nella tabella seguente.

<table><thead><tr class="header"><th>Tipo shader</th><th>Profiles</th></tr></thead><tbody><tr class="odd"><td>Compute Shader</td><td><dl> cs_4_0<br />
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
</dl> Per ulteriori informazioni sul collegamento di shader, vedere <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> e <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>. <br/></td></tr><tr class="odd"><td>Hull shader</td><td><dl> hs_5_0<br />
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
</dl></td></tr><tr class="even"><td>Trama shader</td><td><dl> tx_1_0<br />
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

Per Direct3D 12, vedere [specifica delle firme radice in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [associazione di risorse in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) e [indicizzazione dinamica con HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).

In Direct3D 10 usare l'API per ottenere il profilo vertex, Geometry e pixel shader più adatto a un determinato dispositivo chiamando le funzioni seguenti: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)e [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).

In Direct3D 9 usare i metodi [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) o [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) per recuperare i profili Vertex e pixel shader supportati da un dispositivo. La struttura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) restituita da tali metodi indica i profili Vertex e pixel shader supportati da un dispositivo nei relativi membri **VertexShaderVersion** e **PixelShaderVersion** .

Per esempi, vedere [compilazione con il compilatore corrente](dx-graphics-tools-fxc-using.md).

## <a name="related-topics"></a>Argomenti correlati

* [Effect-strumento compilatore](fxc.md)