---
description: La proprietà Time è l'ora corrente in ore, minuti e secondi come stringa di testo letterale nel formato HH:MM:SS usando un orologio a 24 ore.
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Proprietà Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050d6897b966017a18241ed7e0374174e5343f48f16e311923b1c7564f012681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141793"
---
# <a name="time-property"></a>Proprietà Time

La **proprietà Time** è l'ora corrente in ore, minuti e secondi come stringa di testo letterale nel formato HH:MM:SS usando un orologio a 24 ore. Ad esempio, l'ora 18:57 è rappresentato da "18:57:00". Il formato del valore dipende dalle impostazioni locali dell'utente ed è il formato ottenuto usando la funzione [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) con l'opzione TIME \_ FORCE24HOURFORMAT \| TIME \_ NOTIMEMARKER. Il valore di questa proprietà viene impostato dal programma di installazione Windows e non dall'autore del pacchetto.

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

 

 
