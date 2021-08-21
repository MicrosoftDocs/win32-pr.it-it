---
description: Le costanti del flag di bit LINETERMMODE descrivono diversi tipi di eventi in una linea telefonica che possono \_ essere indirizzati a un dispositivo terminale.
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: LINETERMMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411c1dd633ff1bef49e08eb127f4145f81f3d6785d07f3566431fe7b5d7e8fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518811"
---
# <a name="linetermmode_-constants"></a>Costanti \_ LINETERMMODE

Le costanti del flag di bit **LINETERMMODE \_** descrivono diversi tipi di eventi in una linea telefonica che possono essere indirizzati a un dispositivo terminale.

<dl> <dt>

<span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**PULSANTI \_ LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta di eventi di pressione del pulsante inviati dal terminale alla riga.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**VISUALIZZAZIONE \_ LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta delle informazioni di visualizzazione inviate dalla riga al terminale.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE \_ HOOKSWITCH**
</dt> <dd> <dl> <dt>



Si tratta di eventi hookswitch inviati dal terminale alla riga.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LAMP \_ LINETERMMODE**
</dt> <dd> <dl> <dt>



Si tratta di eventi lamp inviati dalla riga al terminale.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE \_ MEDIABIDIRECT**
</dt> <dd> <dl> <dt>



Si tratta del flusso multimediale bidirezionale associato a una chiamata sulla riga e sul terminale. Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata non può essere controllato in modo indipendente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE \_ MEDIAFROMLINE**
</dt> <dd> <dl> <dt>



Si tratta del flusso multimediale unidirezionale dalla riga al terminale associato a una chiamata sulla riga. Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata può essere controllato in modo indipendente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE \_ MEDIATOLINE**
</dt> <dd> <dl> <dt>



Si tratta del flusso multimediale unidirezionale dal terminale alla riga associata a una chiamata sulla riga. Usare questo valore quando il routing di entrambi i canali unidirezionali del flusso multimediale di una chiamata può essere controllato in modo indipendente.


</dt> </dl> </dd> <dt>

<span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE \_ RINGER**
</dt> <dd> <dl> <dt>



Si tratta di informazioni di controllo della ringer inviate dal commutatore al terminale.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Queste costanti descrivono le classi di flussi di controllo e informazioni che possono essere instradati direttamente tra un dispositivo linea e un dispositivo terminale (ad esempio un set di telefoni).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




