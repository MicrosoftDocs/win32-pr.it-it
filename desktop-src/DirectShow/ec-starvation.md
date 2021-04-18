---
description: Un filtro non riceve dati sufficienti.
ms.assetid: c9cdfe46-02bb-4ea9-ac58-7d63e03c26d8
title: EC_STARVATION (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988d550b93ecb9a3c2f78f2d07f50a3965be945d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324647"
---
# <a name="ec_starvation"></a>scadenza \_ EC

Un filtro non riceve dati sufficienti.

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

L'evento non viene inviato all'applicazione. Se il grafico del filtro è in esecuzione, il gestore del grafico del filtro sospende il grafico e attende il completamento della sospensione. Quindi esegue di nuovo il grafico. Il filtro che invia l'evento non deve completare la transizione alla sospensione fino a quando non dispone di dati sufficienti da riprendere. Se il grafico del filtro non è in esecuzione, il gestore del grafico del filtro ignorerà questo evento.

## <a name="remarks"></a>Commenti

Un parser o un filtro di origine può inviare questo evento se sono in arrivo dati troppo piccoli.

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

 

 




