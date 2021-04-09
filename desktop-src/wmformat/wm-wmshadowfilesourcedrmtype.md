---
title: WM/WMShadowFileSourceDRMType (Windows Media Format 11 SDK)
description: L'attributo WM/WMShadowFileSourceDRMType contiene il tipo di Rights Management usato per proteggere il file originale da cui il file ASF è derivato.
ms.assetid: 58e7a383-6e80-42fc-bc75-5920dbe67a40
keywords:
- Formato di Windows Media WM/WMShadowFileSourceDRMType
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceDRMType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f33d961e8cd3645e4949980d91fe4de79119f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047748"
---
# <a name="wmwmshadowfilesourcedrmtype-windows-media-format-11-sdk"></a>WM/WMShadowFileSourceDRMType (Windows Media Format 11 SDK)

L'attributo **WM/WMShadowFileSourceDRMType** contiene il tipo di Rights Management usato per proteggere il file originale da cui il file ASF è derivato.

## <a name="global-constant"></a>Costante globale

g \_ wszWMWMShadowFileSourceDRMType

## <a name="data-type"></a>Tipo di dati

**\_stringa di tipo WMT \_**

## <a name="remarks"></a>Commenti

Il contenuto presente in un formato di file diverso da ASF ed è protetto con una sorta di Rights Management può essere convertito in un file Windows Media protetto da DRM di Windows Media tramite un processo denominato importazione delle licenze. Un file ASF di questo tipo deve contenere questo attributo e WM/WMShadowFileSourceFileType per tenere traccia del punto da cui proviene il contenuto.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elenco degli attributi**](attribute-list.md)
</dt> </dl>

 

 




