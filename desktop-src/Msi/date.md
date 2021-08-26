---
description: La proprietà Date è il mese, il giorno e l'anno correnti come stringa di testo letterale nel formato MM/GG/AAAA.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: proprietà Date
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf76df99c5567351ddd4d36d1aaad56c8a4d1f385f21ca977a4d54916ce99a4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129631"
---
# <a name="date-property"></a>proprietà Date

La **proprietà Date** è il mese, il giorno e l'anno correnti come stringa di testo letterale nel formato MM/GG/AAAA. Ad esempio, la data 22 giugno 2005 può essere rappresentata come "22/06/2005". Il formato del valore dipende dalle impostazioni locali dell'utente ed è il formato ottenuto usando [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) con l'opzione DATE \_ SHORTDATE. Il valore di questa proprietà viene impostato dal programma di installazione Windows e non dall'autore del pacchetto.

## <a name="remarks"></a>Commenti

Poiché si tratta di una stringa di testo, non può essere usata nelle espressioni condizionali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

