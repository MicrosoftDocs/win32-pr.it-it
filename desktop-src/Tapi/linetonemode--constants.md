---
description: Le \_ costanti LINETONEMODE descrivono selezioni diverse che vengono usate durante la generazione di toni di riga.
ms.assetid: 7bfc7d4e-2ab3-44ec-a936-f2d7dcfce263
title: Costanti LINETONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e1b5a8d49c927dfa3d5ec87f9a4830a91d79d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325284"
---
# <a name="linetonemode_-constants"></a>\_Costanti LINETONEMODE

Le **\_ costanti LINETONEMODE** descrivono selezioni diverse che vengono usate durante la generazione di toni di riga.

<dl> <dt>

<span id="LINETONEMODE_BEEP"></span><span id="linetonemode_beep"></span>**\_segnale acustico LINETONEMODE**
</dt> <dd> <dl> <dt>



Il tono è un segnale acustico, ad esempio quello usato per annunciare l'inizio di una registrazione. La definizione esatta è il provider di servizi definito.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BILLING"></span><span id="linetonemode_billing"></span>**\_fatturazione LINETONEMODE**
</dt> <dd> <dl> <dt>



Il tono è un tono di informazioni sulla fatturazione, ad esempio un tono di richiesta della carta di credito. La definizione esatta è il provider di servizi definito.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_BUSY"></span><span id="linetonemode_busy"></span>**LINETONEMODE \_ occupato**
</dt> <dd> <dl> <dt>



Il tono è un tono occupato. La definizione esatta è il provider di servizi definito.


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_CUSTOM"></span><span id="linetonemode_custom"></span>**LINETONEMODE \_ personalizzato**
</dt> <dd> <dl> <dt>



Il tono è un tono personalizzato definito dalle frequenze dei componenti, di tipo [**LINEGENERATETONE**](/windows/desktop/api/Tapi/ns-tapi-linegeneratetone).


</dt> </dl> </dd> <dt>

<span id="LINETONEMODE_RINGBACK"></span><span id="linetonemode_ringback"></span>**LINETONEMODE \_ risponder**
</dt> <dd> <dl> <dt>



Il tono è la risponder. La definizione esatta è il provider di servizi definito.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Queste costanti vengono usate per definire i toni da generare inband su una chiamata alla parte remota. Si noti che il rilevamento dei toni non personalizzati non usa queste costanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




