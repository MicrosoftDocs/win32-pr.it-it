---
description: La proprietà date è il mese, il giorno e l'anno correnti come una stringa di testo letterale nel formato MM/gg/aaaa.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: proprietà Date
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330382"
---
# <a name="date-property"></a>proprietà Date

La proprietà **date** è il mese, il giorno e l'anno correnti come una stringa di testo letterale nel formato mm/gg/aaaa. Ad esempio, la data 22 giugno 2005 può essere rappresentata come "06/22/2005". Il formato del valore dipende dalle impostazioni locali dell'utente e è il formato ottenuto usando [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) con l' \_ opzione date shortdate. Il valore di questa proprietà viene impostato dal Windows Installer e non dall'autore del pacchetto.

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

 

