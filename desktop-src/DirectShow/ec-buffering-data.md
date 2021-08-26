---
description: Il grafico sta buffering dei dati o ha interrotto la memorizzazione nel buffer dei dati.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc937973db8435657d131ff4adea83892bf87681bb3db9b7d016565f5c38670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965971"
---
# <a name="ec_buffering_data"></a>EC \_ BUFFERING \_ DATA

Il grafico sta buffering dei dati o ha interrotto la memorizzazione nel buffer dei dati.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**BOOL**) **TRUE** se il grafico inizia a eseguire il buffering oppure **FALSE** se il grafico ha interrotto la memorizzazione nel buffer.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Un filtro può inviare questo evento se deve eseguire il buffer dei dati da un'origine esterna. Ad esempio, potrebbe caricare dati da una rete. L'applicazione può usare questo evento per modificare l'interfaccia utente.

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

 

 




