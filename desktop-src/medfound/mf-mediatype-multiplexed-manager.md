---
description: Fornisce un'istanza di IMFMuxStreamMediaTypeManager che può essere usata per ottenere i tipi di supporti dei sottostream di un'origine multimediale multiplexed e controllare la combinazione di sottostream che vengono multiplexed dall'origine.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: MF_MEDIATYPE_MULTIPLEXED_MANAGER attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe00e8824997a0af89099c7fbaad4a2378b44c3360bad0d4b8808023355da2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973690"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>Attributo MF \_ MEDIATYPE \_ MULTIPLEXED \_ MANAGER

Fornisce un'istanza di [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) che può essere usata per ottenere i tipi di supporti dei sottostream di un'origine multimediale multiplexed e controllare la combinazione di sottostream che vengono multiplexed dall'origine.

## <a name="data-type"></a>Tipo di dati

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Commenti

Passare questo valore in [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per ottenere un'istanza di [**IMFMuxStreamMediaTypeManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
