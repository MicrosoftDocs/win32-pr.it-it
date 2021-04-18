---
description: Notifica all'applicazione lo stato di avanzamento all'apertura di un file di rete.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332204"
---
# <a name="ec_loadstatus"></a>\_LOADSTATUS EC

Notifica all'applicazione lo stato di avanzamento all'apertura di un file di rete.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Codice di stato. Vedere la sezione Osservazioni.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il filtro [WM ASF Reader](wm-asf-reader-filter.md) e il filtro legacy [Windows Media Source](windows-media-source-filter.md) inviano questo evento. Il primo parametro dell'evento ha uno dei valori seguenti.



| Valore                        | Descrizione                                    |
|------------------------------|------------------------------------------------|
| AM \_ LOADSTATUS \_ chiuso       | Il filtro di origine ha chiuso il file.         |
| \_connessione LOADSTATUS \_   | Il filtro di origine si connette al server. |
| \_LOADINGDESCR LOADSTATUS \_ | Non usato.                                      |
| \_LOADINGMCAST LOADSTATUS \_ | Non usato                                       |
| \_individuazione LOADSTATUS \_     | Il filtro di origine sta individuando i dati richiesti.  |
| AM \_ LOADSTATUS \_ aperto         | Il filtro di origine ha aperto il file.         |
| \_apertura LOADSTATUS \_      | Il filtro di origine sta aprendo il file.         |



 

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

 

 




