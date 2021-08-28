---
title: Parametri di creazione dei pool di riquadri
description: Usare i parametri in questa sezione per definire pool di riquadri tramite l'API ID3D11Device CreateBuffer.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7350dc01c845542b97674189a120c0d55db95c282dc80b11fda66230618f99b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119471"
---
# <a name="tile-pool-creation-parameters"></a>Parametri di creazione dei pool di riquadri

Usare i parametri in questa sezione per definire pool di riquadri tramite l'API [**ID3D11Device::CreateBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Dimensione**
</dt> <dd>

Dimensione di allocazione, come multiplo di 64 KB. 0 è valido perché in un secondo momento è possibile usare [**un'operazione ID3D11DeviceContext2::ResizeTilePool.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Flag misc delle risorse supportati**
</dt> <dd>

D3D11 RESOURCE MISC TILE POOL (identifica la risorsa come pool di \_ \_ \_ riquadri), \_ D3D11 \_ RESOURCE \_ MISC \_ SHARED, SHARED \_ \_ KEYEDMUTEX o \_ SHARED \_ NTHANDLE.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilizzo delle risorse supportato**
</dt> <dd>

Solo D3D11 \_ USAGE \_ DEFAULT.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

 




