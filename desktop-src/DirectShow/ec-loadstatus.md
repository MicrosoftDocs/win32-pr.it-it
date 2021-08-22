---
description: Notifica all'applicazione lo stato di avanzamento all'apertura di un file di rete.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499f05a26f3fa1387347929f5c14a64b1f440a53ed9b5fd17830d582fb640c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015939"
---
# <a name="ec_loadstatus"></a>EC \_ LOADSTATUS

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

Il [filtro lettore ASF WM](wm-asf-reader-filter.md) e il filtro legacy Windows media [source](windows-media-source-filter.md) inviano questo evento. Il primo parametro dell'evento ha uno dei valori seguenti.



| Valore                        | Descrizione                                    |
|------------------------------|------------------------------------------------|
| AM \_ LOADSTATUS \_ CLOSED       | Il filtro di origine ha chiuso il file.         |
| AM \_ LOADSTATUS \_ CONNECTING   | Il filtro di origine si connette al server. |
| AM \_ LOADSTATUS \_ LOADINGDESCR | Non usato.                                      |
| AM \_ LOADSTATUS \_ LOADINGMCAST | Non usato                                       |
| INDIVIDUAZIONE \_ DI LOADSTATUS \_ AM     | Il filtro di origine sta individuando i dati richiesti.  |
| AM \_ LOADSTATUS \_ OPEN         | Il filtro di origine ha aperto il file.         |
| AM \_ LOADSTATUS \_ OPENING      | Il filtro di origine sta aprendo il file.         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




