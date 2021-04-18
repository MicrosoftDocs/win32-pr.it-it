---
description: Fornisce un'istanza di IMFMuxStreamSampleManager che viene utilizzata per accedere alla raccolta di campioni dai sottoflussi di un'origine multimediale multifunzione.
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: Attributo MFSampleExtension_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b46c277265538ccb2b990ea9d912b9337bcd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310240"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a>\_ \_ Attributo Gestione multiplex MFSampleExtension

Fornisce un'istanza di [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) che viene utilizzata per accedere alla raccolta di campioni dai sottoflussi di un'origine multimediale multifunzione.

## <a name="data-type"></a>Tipo di dati

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Commenti

Passare questo valore in [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per ottenere un'istanza di [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
