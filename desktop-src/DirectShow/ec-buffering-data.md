---
description: Il grafico memorizza nel buffer i dati o ha interrotto il buffering dei dati.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328471"
---
# <a name="ec_buffering_data"></a>\_dati di buffering EC \_

Il grafico memorizza nel buffer i dati o ha interrotto il buffering dei dati.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **True** se il grafico sta iniziando a memorizzare nel buffer oppure **false** se il grafico ha interrotto il buffering.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Un filtro può inviare questo evento se è necessario che i dati vengano memorizzati nel buffer da un'origine esterna. È possibile, ad esempio, caricare i dati da una rete. L'applicazione può utilizzare questo evento per modificare l'interfaccia utente.

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

 

 




