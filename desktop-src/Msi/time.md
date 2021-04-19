---
description: "La proprietà Time è l'ora corrente in ore, minuti e secondi come una stringa di testo letterale nel formato HH: MM: SS usando un clock a 24 ore."
ms.assetid: 6f487e46-e178-4d41-b6fa-7c16aa1c46fd
title: Proprietà Time
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c3456063842c8dd89fadf5860733b5c5aecbef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330139"
---
# <a name="time-property"></a>Proprietà Time

La proprietà **Time** è l'ora corrente in ore, minuti e secondi come una stringa di testo letterale nel formato HH: mm: SS usando un clock a 24 ore. Ad esempio, l'ora 6:57 è rappresentato da "18:57:00". Il formato del valore dipende dalle impostazioni locali dell'utente e è il formato ottenuto usando la funzione [**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) con l' \_ opzione Time FORCE24HOURFORMAT \| time \_ NOTIMEMARKER. Il valore di questa proprietà viene impostato dal Windows Installer e non dall'autore del pacchetto.

## <a name="remarks"></a>Commenti

Poiché si tratta di una stringa di testo, non può essere utilizzata nelle espressioni condizionali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 
