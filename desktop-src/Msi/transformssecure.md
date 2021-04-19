---
description: L'impostazione della proprietà TRANSFORMSSECURE su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Proprietà TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333023"
---
# <a name="transformssecure-property"></a>Proprietà TRANSFORMSSECURE

L'impostazione della proprietà **TRANSFORMSSECURE** su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura. L'impostazione di questa proprietà è simile all'impostazione del [criterio TRANSFORMSSECURE](transformssecure-policy.md) , ad eccezione del fatto che l'ambito è diverso. L'impostazione del criterio TransformsSecure si applica a tutti i pacchetti installati da un determinato utente. L'impostazione della proprietà **TRANSFORMSSECURE** si applica al pacchetto indipendentemente dall'utente.

Lo scopo di questa proprietà è fornire un'archiviazione sicura delle trasformazioni con gli utenti in viaggio di Windows 2000. Quando questa proprietà è impostata, un' [installazione di manutenzione](maintenance-installation.md) può utilizzare solo la trasformazione dal percorso specificato. Se il percorso non è disponibile, l'installazione di manutenzione ha esito negativo. Un'origine per ogni trasformazione protetta deve quindi risiedere nel percorso dell'origine del pacchetto di installazione. Se il programma di installazione rileva che la trasformazione non è presente nel computer locale, è possibile ripristinare la trasformazione da questa origine.

## <a name="remarks"></a>Commenti

Windows Installer interpreta la proprietà [**TRANSFORMSATSOURCE**](transformsatsource.md) in modo che corrisponda alla proprietà **TRANSFORMSSECURE** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Trasformazioni di database](database-transforms.md)
</dt> </dl>

 

 




