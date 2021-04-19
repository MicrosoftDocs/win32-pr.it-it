---
description: L'utente ha terminato la riproduzione.
ms.assetid: 974a9c3e-cfc9-4608-9f98-732aeaa0a752
title: EC_USERABORT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bab4f76e90d7e5f51655eda6dc72834053df87b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328335"
---
# <a name="ec_userabort"></a>\_USERABORT EC

L'utente ha terminato la riproduzione.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuna. L'applicazione deve decidere se arrestare il grafo.

## <a name="remarks"></a>Commenti

Questo codice di evento segnala che l'utente ha terminato la riproduzione normale dei grafici. Ad esempio, i renderer video inviano questo evento se l'utente chiude la finestra del video.

Dopo l'invio di questo evento, il filtro deve rifiutare tutti gli esempi e non inviare alcun evento di [**\_ ridisegno EC**](ec-repaint.md) , fino a quando il filtro non viene interrotto e non viene reimpostato.

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

 

 




