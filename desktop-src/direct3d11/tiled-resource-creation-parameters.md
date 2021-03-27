---
title: Parametri per la creazione di risorse affiancate
description: Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag di varie risorse di D3D11 \_ \_ \_ . In questa sezione vengono forniti i parametri validi per la creazione di risorse affiancate.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719330"
---
# <a name="tiled-resource-creation-parameters"></a>Parametri per la creazione di risorse affiancate

Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag di [**\_ \_ varie \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) risorse di d3d11. In questa sezione vengono forniti i parametri validi per la creazione di risorse affiancate.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Tipo di risorsa supportato**
</dt> <dd>

\[Matrice Texture2D \] (inclusa \[ la matrice TextureCube \] , che è una variante della \[ matrice Texture2D \] ) o un buffer.

**Non supportato:** Texture1D \[ array \] o Texture3D, ma Texture3D potrebbe essere supportato in futuro.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilizzo risorse supportato**
</dt> <dd>

\_ \_ Impostazione predefinita utilizzo d3d11.

**Non supportato:** D3D11 \_ utilizzo \_ dinamico, \_ \_ gestione temporanea utilizzo D3D11 o utilizzo d3d11 non \_ \_ modificabile.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Flag varie delle risorse supportate**
</dt> <dd>

\_Risorse d3d11 \_ varie \_ affiancate (per definizione), \_ varie \_ TEXTURECUBE, argomenti di \_ DRAWINDIRECT \_ , \_ buffer \_ consentono viste non \_ elaborate \_ , struttura del \_ buffer \_ , clamp di \_ risorse \_ o \_ genera \_ MIPS.

**Non supportato:** \_ SHARED, \_ Shared \_ KEYEDMUTEX, \_ GDI \_ compatible, \_ Shared \_ NTHANDLE, \_ Restricted \_ Content, \_ Restrict \_ Shared \_ Resource, \_ Restrict \_ Shared \_ Resource \_ driver, \_ guarded o \_ tile \_ pool.

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Flag di binding supportati**
</dt> <dd>

D3D11 \_ associare la \_ \_ risorsa shader, la \_ \_ destinazione di rendering, il \_ Depth \_ stencil o \_ \_ l'accesso non ordinato.

**Non supportato:** \_ \_Buffer costante, \_ buffer di Vertex \_ \[ Nota che l'associazione di un buffer affiancato come SRV/UAV/RTV è ancora OK \] , buffer di \_ indice \_ , output del \_ flusso \_ , \_ \_ decodificatore di binding o \_ \_ \_ codificatore video bind.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Formati supportati**
</dt> <dd>

Tutti i formati che sarebbero disponibili per la configurazione specificata, indipendentemente dal fatto che vengano affiancati, con alcune eccezioni.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**SampleDesc supportati (conteggio multisample, qualità)**
</dt> <dd>

Qualunque sia il supporto per la configurazione specificata, indipendentemente dal fatto che venga affiancato, con alcune eccezioni.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Larghezza/altezza/MipLevels/ArraySize supportati**
</dt> <dd>

Extent completi supportati da Direct3D 11. Le risorse affiancate non hanno la restrizione sulla dimensione totale della memoria imposta sulle risorse non affiancate. Le risorse affiancate sono limitate solo da limiti di spazio degli indirizzi virtuali complessivi. Per informazioni, vedere [spazio degli indirizzi disponibile per le risorse affiancate](address-space-available-for-tiled-resources.md).

</dd> </dl>

Il contenuto iniziale della memoria del pool di riquadri non è definito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

 




