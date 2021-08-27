---
description: Definisce gli ID risorsa per le risorse stringa condivise.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Resource_Id enumerazione
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5012a6dc40f47a396139eb29f2f88151b4a10ffb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623157"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span id="vspixengine.resource_id"></span>Enumerazione \_ dell'ID risorsa

Definisce gli ID risorsa per le risorse stringa condivise. Questi vengono passati al motore di acquisizione dall'host. Vengono usate per visualizzare le stringhe nella sovrimpressione HUD dell'app acquisita o per passare i valori del Registro di Visual Studio opzioni all'engi di acquisizione

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**MOTORE \_ IDSDISCONNECTED**  
Non usato. ID risorsa per la stringa usata in precedenza per indicare che printscreen è stato raggiunto dopo il completamento della sessione di acquisizione.

<span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR \_ RCDATA1**  
Non usato.

<span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**IDS \_ DEFAULTEXPFILE \_ CONTENT**  
Non usato. ID risorsa per la stringa usata in precedenza per i dati XML negli scenari di acquisizione legacy.

<span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**MESSAGGIO DI ACQUISIZIONE \_ \_ IDS**  
ID risorsa per la stringa "Captured frame".

<span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**ACQUISIZIONE DI \_ \_ IDS NON \_ SUPPORTATA**  
ID risorsa per la stringa "This program has indicated that it cannot be used with Diagnostica della grafica tools".

<span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**IDS CAPTURE NOT SUPPORTED TITLE (TITOLO ACQUISIZIONE IDS \_ \_ NON \_ \_ SUPPORTATO)**  
ID risorsa per la stringa "Funzionalità non supportata"

<span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**FUNZIONALITÀ \_ IDS \_ NON \_ SUPPORTATA**  
ID risorsa per la stringa "Livello di funzionalità del dispositivo non supportato"

<span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**IDS \_ DXVERSION \_ NON \_ SUPPORTATO**  
ID risorsa per la stringa "DirectX version not capturable"

<span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**DCOMP \_ IDS \_ NON \_ SUPPORTATO**  
ID risorsa per la stringa "DCOMP in uso dall'app ma non supportato in questo sistema operativo"

<span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**SCRITTURA IDS \_ \_ NON \_ SUPPORTATA**  
ID risorsa per la stringa "DWRITE in uso dall'app ma non supportato in questo sistema operativo"

<span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**FORMATO DEGLI ERRORI PREVISTI PER GLI \_ \_ \_ ID**  
L'ID risorsa per la stringa "%s ha restituito un errore durante la riproduzione. (HRESULT=%s) \\ r \\ n".

<span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**IDS \_ CAPTURETOOLTIP \_ MESSAGE**  
ID risorsa per la stringa "Use 'Print Screen' key to capture a frame".

<span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**IDS \_ D2D \_ E \_ D10 \_ NON \_ SUPPORTATI**  
ID risorsa per la stringa "D2D e D10 non supportati insieme in questo sistema operativo"

<span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**STATISTICHE \_ HUD IDS \_**  
ID risorsa per la stringa "Frames captured %d. Tempo dell'intervallo (ms) %0,00f"

<span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**METODO INTERNO \_ \_ IDS**  
ID risorsa per la stringa "Metodo interno Directx"

<span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**CONTRASSEGNO DEL \_ FRAME DI \_ ACQUISIZIONE \_ IDS**  
ID risorsa per la stringa "Captured Frame %ld"

<span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**INPUT DI \_ PIPELINESTAGEASSEMBLER**  
Non usato.

<span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE \_ VERTEXSHADER**  
Non usato.

<span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE \_ HULLSHADER**  
Non usato.

<span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE \_ TESSELATOR**  
Non usato.

<span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE \_ DOMAINSHADER**  
Non usato.

<span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE \_ GEOMETRYSHADER**  
Non usato.

<span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE \_ STREAMOUTPUT**  
Non usato.

<span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**\_RASTERIZZAZIONE PIPELINESTAGE**  
Non usato.

<span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE \_ PIXELSHADER**  
Non usato.

<span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE \_ OUTPUTMERGER**  
Non usato.

<span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE \_ COMPUTESHADER**  
Non usato.

<span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT \_ SUPPORTEDFORMAT**  
Non usato.

<span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT \_ CURRENTFORMAT**  
Non usato.

<span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**INTESTAZIONE \_ BUFFEROBJECT**  
Non usato.

<span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT \_ LINE**  
Non usato.

<span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT \_ INVALIDFORMAT**  
Non usato.

<span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT \_ INVALIDEMPTYFORMAT**  
Non usato.

<span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT \_ INVALIDFORMATSIZE**  
Non usato.

<span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO \_ TARGETAPPLICATION**  
Testo visualizzato nella finestra delle proprietà vsglog - Applicazione di destinazione

<span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**PERCORSO \_ SUMMARYINFO**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Percorso

<span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO \_ TARGETVERSION**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Versione di destinazione

<span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO \_ LASTMODIFIEDDATE**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Data ultima modifica

<span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO \_ PROCESSID**  
Testo visualizzato nel file vsglog Finestra Proprietà - ID processo

<span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO \_ EXPERIMENTFILE**  
Testo visualizzato nel file vsglog Finestra Proprietà - File esperimento

<span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO \_ RUNFILE**  
Testo visualizzato nel file vsglog Finestra Proprietà - Esegui file

<span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**DIMENSIONI \_ SUMMARYINFO**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Dimensioni

<span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO \_ CREATEDBYPIXVERSION**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Creato dalla versione

<span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO \_ SESSIONSTARTTIME**  
Testo visualizzato nell'elenco vsglog Finestra Proprietà - Ora di inizio sessione

<span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**  
Testo visualizzato nel Finestra Proprietà vsglog - System Information

<span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**PROCESSORE SUMMARYINFO \_**  
Testo visualizzato nel Finestra Proprietà vsglog - Processore

<span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**MEMORIA \_ SUMMARYINFO**  
Testo visualizzato nel Finestra Proprietà vsglog - Memoria

<span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO \_ OSVERSION**  
Testo visualizzato nel Finestra Proprietà vsglog - Versione del sistema operativo

<span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO \_ OSARCHITECTURE**  
Testo visualizzato nel Finestra Proprietà vsglog - Architettura del sistema operativo

<span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO \_ TARGETAPPARCHITECTURE**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Architettura dell'app di destinazione

<span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO \_ MAXHWFEATURELEVEL**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Livello massimo funzionalità hardware

<span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**DRIVER \_ SUMMARYINFOCONCURRENTCREATES**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Creazione simultanea del driver

<span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO \_ DRIVERCOMMANDLISTS**  
Testo visualizzato nel file vsglog Finestra Proprietà - Elenchi di comandi del driver

<span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO \_ DOUBLEPRECISIONSHADERS**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Shader con precisione doppia

<span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO \_ DIRECTCOMPUTECS4X**  
Testo visualizzato nel Finestra Proprietà vsglog - Direct Compute CS 4.x

<span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO \_ 10BITXRHIGHCOLORFORMAT**  
Testo visualizzato nel Finestra Proprietà vsglog - 10BITXRHIGHCOLORFORMAT

<span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO \_ EXTENDEDCOLORFORMATSUPPORT**  
Testo visualizzato nel Finestra Proprietà vsglog - Supporto del formato colori esteso

<span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO \_ DISPLAYINFORMATION**  
Testo visualizzato nella finestra di dialogo vsglog Finestra Proprietà - Visualizzare le informazioni

<span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO \_ DISPLAYNINFORMATION**  
Testo visualizzato nel Finestra Proprietà vsglog - Visualizza N informazioni

<span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**NOME \_ SUMMARYINFO**  
Testo visualizzato nel Finestra Proprietà vsglog - Nome

<span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO \_ DESCRIPTION**  
Testo visualizzato nel Finestra Proprietà vsglog - Descrizione

<span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO \_ DISPLAYMEMORY**  
Testo visualizzato nel Finestra Proprietà vsglog - Visualizza memoria

<span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO \_ DRIVERNAME**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Nome driver

<span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO \_ DRIVERVERSION**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Versione del driver

<span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO \_ MODULEINFORMATION**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Informazioni sul modulo

<span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO \_ DIRECT3DINFORMATION**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Informazioni direct3D

<span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO \_ VSGVERSION**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Versione vsg

<span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO \_ CAPTUREMACHINE**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Acquisisci computer

<span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO \_ PLAYBACKMACHINE**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Macchina per la riproduzione

<span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO \_ REMOTEDATA**  
Testo visualizzato nel Finestra Proprietà vsglog - Dati remoti

<span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO \_ OtherDirect3DInformation**  
Testo visualizzato nel Finestra Proprietà vsglog - Altre informazioni Direct3D

<span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO \_ SIZEGB**  
Testo visualizzato nel Finestra Proprietà vsglog - Dimensioni GB

<span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO \_ SIZEMB**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Dimensioni MB

<span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO \_ SIZEBYTES**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Byte di dimensioni

<span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO \_ MEMORYMB**  
Testo visualizzato nel file vsglog Finestra Proprietà - MB di memoria

<span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ X86**  
Testo visualizzato nel Finestra Proprietà vsglog - X86

<span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ X64**  
Testo visualizzato nel Finestra Proprietà vsglog - X64

<span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ TRUE**  
Testo visualizzato nel Finestra Proprietà vsglog - True

<span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ FALSE**  
Testo visualizzato nel Finestra Proprietà vsglog - False

<span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO \_ ARM32**  
Testo visualizzato nel Finestra Proprietà vsglog - ARM 32

<span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO \_ UNKNOWNCPUARCHITECTURE**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Architettura CPU sconosciuta

<span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO \_ AllDXGIFormatValues**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Tutti i valori di formato DXGI

<span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO \_ AllD3D11FormatSupportValues**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Tutti i valori di supporto del formato D3D11

<span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**THREADING DELLE \_ FUNZIONALITÀ SUMMARYINFO D3D11 \_ \_**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - D3D11 \_ FEATURE \_ THREADING

<span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO \_ DriverConcurrentCreates1**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Creazione simultanea del driver 1

<span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO \_ DriverCommandLists1**  
Testo visualizzato nel file vsglog Finestra Proprietà - Elenchi di comandi del driver 1

<span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**LA FUNZIONALITÀ SUMMARYINFO \_ D3D11 \_ \_ RADDOPPIA**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - D3D11 \_ FEATURE \_ DOUBLES

<span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO \_ DoublePrecisionFloatShaderOps**  
Testo visualizzato nel file vsglog Finestra Proprietà - Double Precision Float Shader Ops

<span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D10 \_ X OPZIONI \_ HARDWARE \_**  
Testo visualizzato nella finestra di dialogo vsglog Finestra Proprietà - D3D11 \_ FEATURE \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS

<span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ Via Shader \_ \_ 4 \_ x**  
Testo visualizzato nel Finestra Proprietà vsglog - ComputeShaders + Raw e Structure dBuffers tramite Shader 4.x

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**OPZIONI DI SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D11 \_**  
Testo visualizzato nella finestra di dialogo vsglog Finestra Proprietà - D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS

<span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO \_ OutputMergerLogicOp**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Output Merger Logic Op

<span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO \_ UAVOnlyRenderingForcedSampleCount**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Conteggio campioni forzati solo per il rendering UAV

<span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO \_ DiscardAPIsSeenByDriver**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Rimuovere le API visualizzate dal driver

<span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO \_ FlagsForUpdateAndCopySeenByDriver**  
Testo visualizzato nel file vsglog Finestra Proprietà - Flag per l'aggiornamento e la copia visualizzati dal driver

<span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO \_ ClearView**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Cancella visualizzazione

<span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO \_ CopyWithOverlap**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Copia con sovrapposizione

<span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO \_ ConstantBufferPartialUpdate**  
Testo visualizzato nel file vsglog Finestra Proprietà - Aggiornamento parziale del buffer costante

<span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO \_ ConstantBufferOffsetting**  
Testo visualizzato nel file vsglog Finestra Proprietà - Offset costante del buffer

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicConstantBuffer**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Non viene mappata alcuna sovrascrittura nel buffer costante dinamico

<span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO \_ MapNoOverwriteOnDynamicBufferSRV**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Nessuna sovrascrittura del mapping in SRV del buffer dinamico

<span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO \_ MultisampleRTVWithForcedSampleCountOne**  
Testo visualizzato nella finestra di dialogo vsglog Finestra Proprietà - RtV multicampionamento con conteggio campioni forzato 1

<span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ SAD4ShaderInstructions**  
Testo visualizzato nel file vsglog Finestra Proprietà - Istruzioni per shader SAD4

<span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO \_ ExtendedDoublesShaderInstructions**  
Testo visualizzato nel file vsglog Finestra Proprietà - Istruzioni estese per lo shader Double

<span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO \_ ExtendedResourceSharing**  
Testo visualizzato nel file vsglog Finestra Proprietà - Condivisione risorse estesa

<span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**INFORMAZIONI SULL'ARCHITETTURA DELLE FUNZIONALITÀ DI SUMMARYINFO \_ D3D11 \_ \_ \_**  
Testo visualizzato nella finestra di dialogo vsglog Finestra Proprietà - D3D11 FEATURE ARCHITECTURE INFO (INFORMAZIONI SULL'ARCHITETTURA \_ \_ DELLE FUNZIONALITÀ D3D11) \_

<span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO \_ TileBasedDeferredRenderer**  
Testo visualizzato nel rendering Finestra Proprietà vsglog - Renderer posticipato basato su riquadri

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**OPZIONI \_ DELLA FUNZIONALITÀ \_ D3D11 SUMMARYINFO \_ D3D9 \_**  
Testo visualizzato nel file vsglog Finestra Proprietà - OPZIONI \_ D3D11 FEATURE \_ D3D9 \_

<span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO \_ FullNonPow2TextureSupport**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Supporto completo delle trame non Pow2

<span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUPPORTO DELLA PRECISIONE \_ MINIMA DELLO SHADER DELLA FUNZIONALITÀ SUMMARYINFO D3D11 \_ \_ \_ \_ \_**  
Testo visualizzato nel file vsglog Finestra Proprietà - D3D11 \_ FEATURE SHADER MIN PRECISION \_ \_ \_ \_ SUPPORT

<span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO \_ PixelShaderMinPrecision**  
Testo visualizzato nell'oggetto vsglog Finestra Proprietà - Precisione minima pixel shader

<span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO \_ AllOtherShaderStagesMinPrecision**  
Testo visualizzato nel file vsglog Finestra Proprietà - Tutte le altre fasi shader Precisione minima

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 SHADOW SUPPORT (SUPPORTO SHADOW D3D9 PER LA FUNZIONALITÀ SUMMARYINFO D3D11) \_ \_**  
Testo visualizzato nel file vsglog Finestra Proprietà - D3D11 \_ FEATURE \_ D3D9 \_ SHADOW \_ SUPPORT

<span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO \_ SupportsDepthAsTextureWithLessEqualComparisonFilter**  
Testo visualizzato nel filtro vsglog Finestra Proprietà: supporta la profondità come trama con filtro di confronto meno uguale

<span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1**  
Testo visualizzato nel file vsglog Finestra Proprietà - D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS1

<span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO \_ TiledResourcesTier**  
Testo visualizzato nel livello Finestra Proprietà vsglog - Risorse affiancate

<span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO \_ MinMaxFiltering**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Filtro minimo massimo

<span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO \_ ClearViewAlsoSupportsDepthOnlyFormats**  
Il testo visualizzato nella finestra di Finestra Proprietà vsglog - Cancella visualizzazione supporta anche i formati solo profondità

<span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO \_ MapOnDefaultBuffers**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Mapping su buffer predefiniti

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUPPORTO DI ISTANZE SEMPLICI DELLA FUNZIONALITÀ \_ \_ \_ SUMMARYINFO D3D11 D3D9 \_ \_ \_**  
Testo visualizzato nel file vsglog Finestra Proprietà - D3D11 \_ FEATURE \_ D3D9 \_ SIMPLE \_ INSTANCING \_ SUPPORT

<span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO \_ SimpleInstancingSupported0**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Supporto di istanze semplici 0

<span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUPPORTO MARCATORI DI FUNZIONALITÀ SUMMARYINFO \_ D3D11 \_ \_ \_**  
Testo visualizzato nella finestra di dialogo vsglog Finestra Proprietà - SUPPORTO \_ MARCATORI \_ DI FUNZIONALITÀ D3D11 \_

<span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**Profilo \_ SUMMARYINFO**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Profilo

<span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS1**  
Testo visualizzato nel file vsglog Finestra Proprietà - D3D11 \_ FEATURE \_ D3D9 \_ OPTIONS1

<span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO \_ FullNonPow2TextureSupported**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Trama completa non Pow2 supportata

<span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO \_ DepthAsTextureWithLessEqualComparisonFilterSupported**  
Testo visualizzato nel file vsglog Finestra Proprietà - Profondità come trama con filtro di confronto meno uguale supportato

<span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO \_ SimpleInstancingSupported1**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - Istanze semplici supportate 1

<span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO \_ TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**  
Testo visualizzato nella finestra di dialogo vsglog Finestra Proprietà - Destinazione di rendering viso cubo trama con stencil di profondità non cubo supportato

<span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO \_ DXGIFormat**  
Testo visualizzato nel Finestra Proprietà vsglog - DXGIFormat

<span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO \_ DXGIFormat1**  
Testo visualizzato nel Finestra Proprietà vsglog - DXGIFormat1

<span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO \_ MODULENAME**  
Testo visualizzato nella finestra di Finestra Proprietà vsglog - MODULENAME

<span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**CONFIGURAZIONE \_ IDD**  
Testo visualizzato nella finestra di dialogo Configura firewall in VsGraphicsRemoteEngine

<span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**ICONA \_ \_ DELL'INTESTAZIONE STATICA IDC \_**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Icona intestazione statica

<span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**INTESTAZIONE STATICA \_ \_ IDC**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Intestazione statica

<span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**CONFIGURAZIONE \_ \_ FW STATICA \_ IDC**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Configurazione del firewall statico

<span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**ICONA DI \_ FW STATIC \_ IDC \_**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Icona del firewall statico

<span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**INTESTAZIONE \_ \_ FW STATICA IDC \_**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Intestazione firewall statica

<span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC \_ STATIC \_ GROUPBOX \_ FW**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Gruppo statico Firewall casella

<span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC \_ CHECK \_ FW \_ DOMAIN \_ NETWORKS**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Controlla reti di dominio del firewall

<span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC \_ CHECK \_ FW \_ PRIVATE \_ NETWORKS**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Controlla reti private del firewall

<span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC \_ CHECK \_ FW \_ PUBLIC \_ NETWORKS**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Controlla reti pubbliche del firewall

<span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**CONFIGURARE IL PULSANTE IDC \_ \_**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Pulsante Configura

<span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**ID \_ CONFIGURATION \_ CANCEL**  
Testo visualizzato nel controllo della finestra di dialogo Configura firewall - Annullamento configurazione

<span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**IDS \_ TEXT \_ FW \_ NOT \_ CONFIGURED**  
Testo visualizzato nella finestra di dialogo Configura firewall - Firewall di testo non configurato

<span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**IDS \_ TEXT \_ FW \_ CONFIGURED**  
Testo visualizzato nella finestra di dialogo Configura firewall - Firewall di testo configurato

<span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**IDS FIREWALL RULE NAME (NOME REGOLA \_ FIREWALL \_ \_ IDS)**  
Testo visualizzato nella finestra di dialogo Configura firewall - Nome regola firewall

<span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**DESCRIZIONE DELLA REGOLA \_ DEL FIREWALL \_ \_ IDS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Descrizione regola firewall

<span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**INTESTAZIONE \_ STATICA \_ IDS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Intestazione statica

<span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**TITOLO CONFIGURAZIONE \_ \_ IDS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Titolo configurazione

<span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**INTESTAZIONE \_ \_ FW STATICA IDS \_**  
Testo visualizzato nella finestra di dialogo Configura firewall - Intestazione firewall statica

<span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDS \_ STATIC \_ GROUPBOX \_ FW**  
Testo visualizzato nella finestra di dialogo Configura firewall - Gruppo statico Firewall della casella

<span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS \_ CHECK \_ FW \_ DOMAIN \_ NETWORKS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Controllare le reti di dominio del firewall

<span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS \_ CHECK \_ FW \_ PRIVATE \_ NETWORKS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Controlla reti private del firewall

<span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDS \_ CHECK \_ FW \_ PUBLIC \_ NETWORKS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Controllare le reti pubbliche del firewall

<span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**CONFIGURARE IL \_ PULSANTE \_ IDS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Confiture Buttom

<span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**ANNULLAMENTO CONFIGURAZIONE \_ \_ IDS**  
Testo visualizzato nella finestra di dialogo Configura firewall - Annullamento configurazione

<span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**IDS \_ CAPTURETOOLTIP \_ MESSAGE \_ CORESYSTEM**  
ID risorsa per la stringa "Use the capture button in Visual Studio to capture frame(s)."

<span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDS \_ ET \_ NONE**  
Non usato.

<span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**IDS \_ ET \_ SESSIONSTART**  
Non usato.

<span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**IDS \_ ET \_ SESSIONEND**  
Non usato.

<span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**IDS \_ ET \_ PROCESSSTART**  
Non usato.

<span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**IDS \_ ET \_ PROCESSEND**  
Non usato.

<span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**IDS \_ ET \_ FRAMEBEGIN**  
Non usato.

<span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**IDS \_ ET \_ FRAMEEND**  
Non usato.

<span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**IDS \_ ET \_ USEREVENTBEGIN**  
Non usato.

<span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**IDS \_ ET \_ USEREVENTEND**  
Non usato.

<span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**IDS \_ ET \_ USERMARKER**  
Non usato.

<span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**CHIAMATA IDS \_ ET \_**  
Non usato.

<span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**IDS \_ ET \_ OBJECTPOPULATION**  
Non usato.

<span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**IDS \_ ET \_ OBJECTCREATION**  
Non usato.

<span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**IDS \_ ET \_ CALLSYNC**  
Non usato.

<span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDS \_ ET \_ UNKNOWN**  
Non usato.

<span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDS \_ TRIGGER \_ NONE**  
Non usato.

<span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDS \_ TRIGGER \_ PROGRAMSTART**  
Non usato.

<span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**FRAME DEL \_ TRIGGER \_ IDS**  
Non usato.

<span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**ORA \_ TRIGGER \_ IDS**  
Non usato.

<span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDS \_ TRIGGER \_ USERMARKER**  
Non usato.

<span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDS \_ TRIGGER \_ BEGINUSEREVENT**  
Non usato.

<span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDS \_ TRIGGER \_ ENDUSEREVENT**  
Non usato.

<span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**CAPTUREFRAME \_ DEL TRIGGER \_ IDS**  
Non usato.

<span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**\_ \_ APICAPTURE DEL TRIGGER IDS**  
Non usato.

<span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**IDS \_ ERROR \_ CALLDATA**  
Non usato.

<span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**ERRORE IDS \_ \_ CREATINGLOG**  
Non usato.

<span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**IDS \_ UNKNOWNCALL**  
Non usato.

<span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**IDS \_ WARN \_ FEATURE \_ LEVEL \_ CHANGED**  
Non usato.

<span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**FREQUENZA \_ STATO \_ ID**  

<span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ DISABLE \_ HUD**  

<span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID \_ DISABLE \_ COMPAT**  

<span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID \_ COLLECT \_ CALLSTACKS**  

<span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID \_ ENABLE \_ SDKERROR \_ STOP**  

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



