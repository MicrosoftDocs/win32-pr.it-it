---
description: Impostare la proprietà MSINODISABLEMEDIA per impedire al programma di installazione di impostare la proprietà DISABLEMEDIA. L'impostazione della proprietà DISABLEMEDIA impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Proprietà MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330150"
---
# <a name="msinodisablemedia-property"></a>Proprietà MSINODISABLEMEDIA

Impostare la proprietà **MSINODISABLEMEDIA** per impedire al programma di installazione di impostare la proprietà [**DISABLEMEDIA**](-disablemedia.md) . L'impostazione della proprietà **DISABLEMEDIA** impedisce al programma di installazione di registrare qualsiasi origine multimediale, ad esempio un CD-ROM, come origine valida per il prodotto.

Quando **MSINODISABLEMEDIA** non è impostato, il programma di installazione potrebbe aggiungere [**DISABLEMEDIA**](-disablemedia.md) al flusso di proprietà amministrative quando si esegue un' [installazione amministrativa](administrative-installation.md). In questo modo si impedisce agli utenti che eseguono l'installazione dall'immagine amministrativa di eseguire l'installazione da un supporto, ad esempio un CD-ROM.

-   Quando si esegue un'installazione amministrativa, il programma di installazione aggiunge [**DISABLEMEDIA**](-disablemedia.md) al flusso di proprietà amministrative solo se la proprietà di [**Riepilogo dei conteggi delle pagine**](page-count-summary.md) è inferiore a 150.

Se [**DISABLEMEDIA**](-disablemedia.md) è elencato nella proprietà [**AdminProperties**](adminproperties.md) , l'impostazione **MSINODISABLEMEDIA** impedisce l'impostazione di **DISABLEMEDIA** durante un'installazione amministrativa. In questo caso, il programma di installazione può registrare un'origine multimediale e un utente può quindi avere la possibilità di reinstallare dall'origine multimediale se l'immagine di installazione amministrativa originale non è più disponibile in un secondo momento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer su Windows Server 2003, Windows XP e Windows 2000. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




