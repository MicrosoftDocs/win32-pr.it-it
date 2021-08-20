---
description: L'impostazione della proprietà TRANSFORMSSECURE su 1 indica al programma di installazione che le trasformazioni devono essere memorizzate nella cache locale nel computer dell'utente in un percorso in cui l'utente non ha accesso in scrittura.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: TRANSFORMSSECURE - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af3432b8f895d4d9f5d0fe643ef8106e01e28ad64fb2db177e968fbc13d88de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141634"
---
# <a name="transformssecure-property"></a>TRANSFORMSSECURE - proprietà

L'impostazione della proprietà **TRANSFORMSSECURE** su 1 indica al programma di installazione che le trasformazioni devono essere memorizzate nella cache locale nel computer dell'utente in un percorso in cui l'utente non ha accesso in scrittura. L'impostazione di questa proprietà è simile [all'impostazione dei criteri TransformsSecure,](transformssecure-policy.md) ad eccezione del fatto che l'ambito è diverso. L'impostazione dei criteri TransformsSecure si applica a tutti i pacchetti installati da un determinato utente. **L'impostazione della proprietà TRANSFORMSSECURE** si applica al pacchetto indipendentemente dall'utente.

Lo scopo di questa proprietà è fornire l'archiviazione sicura delle trasformazioni con utenti in viaggio di Windows 2000. Quando questa proprietà è impostata, [un'installazione di manutenzione](maintenance-installation.md) può usare solo la trasformazione dal percorso specificato. Se il percorso non è disponibile, l'installazione di manutenzione non riesce. Un'origine per ogni trasformazione protetta deve pertanto risiedere nel percorso dell'origine del pacchetto di installazione. Quindi, se il programma di installazione rileva che la trasformazione non è presente nel computer locale, può ripristinare la trasformazione da questa origine.

## <a name="remarks"></a>Commenti

Windows Il programma di installazione [**interpreta la proprietà TRANSFORMSATSOURCE**](transformsatsource.md) in modo che sia uguale alla **proprietà TRANSFORMSSECURE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Trasformazioni del database](database-transforms.md)
</dt> </dl>

 

 




