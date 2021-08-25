---
description: Fornisce un'istanza di IMFMuxStreamSampleManager usata per accedere alla raccolta di esempi dai sottostream di un'origine multimediale multiplexed.
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: MFSampleExtension_MULTIPLEXED_MANAGER attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848b613c4f6de9086f3da9636a29cad73499b7f0b37bd3445cee3d1086d61d7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848101"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a>Attributo MFSampleExtension \_ MULTIPLEXED \_ MANAGER

Fornisce un'istanza di [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) usata per accedere alla raccolta di esempi dai sottostream di un'origine multimediale multiplexed.

## <a name="data-type"></a>Tipo di dati

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Commenti

Passare questo valore in [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per ottenere un'istanza di [**IMFMuxStreamSampleManager.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
