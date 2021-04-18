---
description: Inviato quando un'applicazione usa il filtro del writer ASF WM per indicizzare i file di Windows Media Video.
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: EC_WMT_INDEX_EVENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327827"
---
# <a name="ec_wmt_index_event-dshowh"></a>EC_WMT_INDEX_EVENT (dshow. h)

Inviato quando un'applicazione usa il filtro del [writer ASF WM](wm-asf-writer-filter.md) per indicizzare i file di Windows Media video.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Può essere uno dei seguenti messaggi **di \_ stato di WMT** .



| Valore                | Descrizione              |
|----------------------|--------------------------|
| WMT \_ avviato         | L'indicizzazione è iniziata.      |
| WMT \_ chiuso          | L'indicizzazione è stata completata.  |
| \_stato dell'indice WMT \_ | L'indicizzazione è in corso. |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Se *lParam1* è WMT \_ Closed o WMT \_ Started, *lParam2* è zero. Se *lParam1* è \_ \_ lo stato di avanzamento dell'indice WMT, *lParam2* è un **valore DWORD** che specifica lo stato di avanzamento corrente come percentuale delle dimensioni totali del download.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




