---
description: Fornisce un'istanza di IMFMuxStreamMediaTypeManager che può essere usata per ottenere i tipi di supporto dei flussi sottoflussi di un'origine multimediale con multiplexing, nonché per controllare la combinazione di sottoflussi multiplexati dall'origine.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: Attributo MF_MEDIATYPE_MULTIPLEXED_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104234488"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>\_Attributo di \_ Gestione multiplex MF MEDIATYPE \_

Fornisce un'istanza di [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) che può essere usata per ottenere i tipi di supporto dei flussi sottoflussi di un'origine multimediale con multiplexing, nonché per controllare la combinazione di sottoflussi multiplexati dall'origine.

## <a name="data-type"></a>Tipo di dati

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>Commenti

Passare questo valore in [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) per ottenere un'istanza di [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
