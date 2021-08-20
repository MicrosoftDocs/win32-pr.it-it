---
title: Parametri di creazione di risorse affiancate
description: Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag D3D11 \_ RESOURCE \_ MISC \_ TILED. Questa sezione fornisce i parametri validi per la creazione di risorse affiancate.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9668c21060cbb8f39884204780ce689b3e67196aef0bdcfef891836768f04af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279841"
---
# <a name="tiled-resource-creation-parameters"></a>Parametri di creazione di risorse affiancate

Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILED.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Questa sezione fornisce i parametri validi per la creazione di risorse affiancate.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo di risorsa supportato**
</dt> <dd>

Matrice Texture2D \[ \] (inclusa la matrice TextureCube, che \[ è una variante della matrice \] Texture2D) \[ o \] buffer.

**NON supportato:** Matrice Texture1D \[ \] o Texture3D, ma Texture3D potrebbe essere supportato in futuro.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilizzo delle risorse supportato**
</dt> <dd>

D3D11 USAGE DEFAULT (IMPOSTAZIONE PREDEFINITA UTILIZZO D3D11). \_ \_

**NON supportato:** D3D11 \_ USAGE \_ DYNAMIC, D3D11 \_ USAGE STAGING o \_ D3D11 \_ USAGE \_ IMMUTABLE.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Flag di errore delle risorse supportati**
</dt> <dd>

D3D11 \_ RESOURCE \_ MISC \_ TILED (per definizione), \_ MISC \_ TEXTURECUBE, \_ DRAWINDIRECT \_ ARGS, \_ BUFFER ALLOW RAW \_ \_ \_ VIEWS, BUFFER \_ STRUCTURED, RESOURCE CLAMP o GENERATE \_ \_ \_ \_ \_ MIPS.

**NON supportato:** \_ SHARED, \_ SHARED \_ KEYEDMUTEX, \_ GDI \_ COMPATIBLE, \_ SHARED \_ NTHANDLE, \_ RESTRICTED CONTENT, RESTRICT SHARED \_ \_ \_ \_ RESOURCE, RESTRICT SHARED RESOURCE \_ \_ \_ \_ DRIVER, \_ GUARDED O \_ TILE \_ POOL.

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Flag di associazione supportati**
</dt> <dd>

RISORSA BIND SHADER D3D11, \_ \_ DESTINAZIONE DI \_ \_ \_ RENDERING, STENCIL DI PROFONDITÀ \_ O ACCESSO NON \_ \_ \_ ORDINATO.

**NON supportato:** \_ CONSTANT BUFFER, VERTEX BUFFER si noti che l'associazione di un buffer affiancato come \_ \_ \_ \[ SRV/UAV/RTV è ancora \] ok, \_ INDEX \_ BUFFER, \_ STREAM \_ OUTPUT, BIND DECODER o \_ BIND VIDEO \_ \_ \_ \_ ENCODER.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formati supportati**
</dt> <dd>

Tutti i formati disponibili per la configurazione specificata, indipendentemente dal fatto che venga affiancata, con alcune eccezioni.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc supportato (conteggio multicampionamento, qualità)**
</dt> <dd>

Qualsiasi elemento sia supportato per la configurazione specificata, indipendentemente dal fatto che venga affiancata, con alcune eccezioni.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Larghezza/altezza supportata/MipLevels/ArraySize**
</dt> <dd>

Extent completi supportati da Direct3D 11. Le risorse affiancate non hanno la restrizione sulle dimensioni totali della memoria imposte alle risorse non affiancate. Le risorse affiancate sono vincolate solo dai limiti complessivi dello spazio degli indirizzi virtuali. Per informazioni, vedere [Spazio indirizzi disponibile per le risorse affiancate.](address-space-available-for-tiled-resources.md)

</dd> </dl>

Il contenuto iniziale della memoria del pool di riquadri non è definito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

 




