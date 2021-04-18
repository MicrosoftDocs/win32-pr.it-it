---
description: Le \_ costanti del flag di bit LINETERMMODE descrivono i diversi tipi di eventi su una linea telefonica che possono essere indirizzati a un dispositivo terminale.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Costanti LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326879"
---
# <a name="linetermmode_-constants"></a>\_Costanti LINETERMMODE

Le costanti del flag di bit **LINETERMMODE \_** descrivono i diversi tipi di eventi su una linea telefonica che possono essere indirizzati a un dispositivo terminale.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**\_pulsanti LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta di eventi di pressione del pulsante inviati dal terminale alla riga.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**\_visualizzazione LINETERMMODE**
</dt> <dd> <dl> <dt>



Vengono visualizzate le informazioni inviate dalla riga al terminale.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**\_HOOKSWITCH LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta di eventi hookswitch inviati dal terminale alla riga.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**\_lampade LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta di eventi Lamp inviati dalla riga al terminale.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**\_MEDIABIDIRECT LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta del flusso multimediale bidirezionale associato a una chiamata sulla riga e sul terminale. Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata non può essere controllato in modo indipendente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**\_MEDIAFROMLINE LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta del flusso multimediale unidirezionale dalla riga al terminale associato a una chiamata sulla riga. Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata può essere controllato in modo indipendente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**\_MEDIATOLINE LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta del flusso multimediale unidirezionale dal terminale alla riga associata a una chiamata sulla riga. Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata può essere controllato in modo indipendente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ Ringer**
</dt> <dd> <dl> <dt>



Si tratta di informazioni di controllo suoneria inviate dal passaggio al terminale.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Queste costanti descrivono le classi di flussi di controllo e di informazioni che possono essere indirizzate direttamente tra un dispositivo a linee e un dispositivo Terminal (ad esempio un set di telefono).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




