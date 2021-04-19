---
description: Il grafico apre un file o ha terminato l'apertura di un file.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332196"
---
# <a name="ec_opening_file"></a>\_file di apertura EC \_

Il grafico apre un file o ha terminato l'apertura di un file.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**True** se il grafico sta iniziando ad aprire un file oppure **false** se il grafo non sta più aprendo il file.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Un filtro può inviare questo evento se trascorre molto tempo per l'apertura di un file. Ad esempio, il file potrebbe trovarsi in una rete. L'applicazione può utilizzare questo evento per modificare l'interfaccia utente.

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

 

 




