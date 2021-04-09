---
description: L'impostazione del criterio TransformsSecure su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Criteri di TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878546"
---
# <a name="transformssecure-policy"></a>Criteri di TransformsSecure

L'impostazione del criterio TransformsSecure su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura. L'impostazione di questo criterio equivale all'impostazione della [Proprietà TRANSFORMSSECURE](transformssecure.md) , ad eccezione del fatto che l'ambito è diverso. L'impostazione del criterio TransformsSecure si applica a tutti i pacchetti installati in un determinato computer. L'impostazione della proprietà TRANSFORMSSECURE si applica al pacchetto indipendentemente dal computer.

Lo scopo di questo criterio è fornire un'archiviazione sicura delle trasformazioni con gli utenti in viaggio di Windows 2000. A partire da Windows Server 2003, il valore predefinito di questo criterio è 1.

Quando questo criterio è impostato, un' [installazione di manutenzione](maintenance-installation.md) può utilizzare la trasformazione solo dalla cache protetta. Nel caso in cui il programma di installazione rilevi che la trasformazione non è presente nel computer locale, il programma di installazione tenta di ripristinare la trasformazione. Per consentire al programma di installazione di ripristinare la trasformazione, la trasformazione protetta deve trovarsi in un'origine autorizzata nell'elenco di origine del pacchetto di installazione. Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md). L'installazione di manutenzione ha esito negativo se la trasformazione non è disponibile o non può essere caricata.

In Windows Server 2003, se questo criterio non è impostato, il comportamento predefinito consiste nell'archiviare le trasformazioni in una posizione sicura. In tutte le versioni precedenti a Windows Server 2003, se il criterio non è impostato, il comportamento predefinito consiste nell'archiviare le trasformazioni nel profilo utenti.

Per ulteriori informazioni, vedere anche [trasformazioni protette](secured-transforms.md) .

Windows Installer interpreta il [criterio TransformsAtSource](transformsatsource-policy.md) in modo che corrisponda al criterio TRANSFORMSSECURE.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



