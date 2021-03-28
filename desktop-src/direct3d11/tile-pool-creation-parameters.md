---
title: Parametri di creazione dei pool di riquadri
description: Usare i parametri in questa sezione per definire i pool di sezioni tramite l'API CreateBuffer di ID3D11Device.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044235"
---
# <a name="tile-pool-creation-parameters"></a>Parametri di creazione dei pool di riquadri

Usare i parametri in questa sezione per definire i pool di sezioni tramite l'API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Dimensioni**
</dt> <dd>

Dimensioni di allocazione, come un multiplo di 64KB. 0 è valido perché in seguito è possibile usare un'operazione [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Flag varie delle risorse supportate**
</dt> <dd>

\_ \_ \_ \_ Il pool di sezioni varie della risorsa d3d11 (identifica la risorsa come pool di sezioni), la \_ risorsa d3d11 \_ varie \_ condivise, \_ \_ KEYEDMUTEX condivise o \_ \_ NTHANDLE condiviso.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilizzo risorse supportato**
</dt> <dd>

\_Solo utilizzo \_ predefinito di d3d11.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

 




