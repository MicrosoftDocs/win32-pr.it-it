---
description: L'impostazione del criterio TransformsSecure su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache locale nel computer dell'utente in un percorso in cui l'utente non ha accesso in scrittura.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: TransformsSecure Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6300a25db8e80003ff2a03afd56b168b9697f92764f16a26e99860c0a27796bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500297"
---
# <a name="transformssecure-policy"></a>TransformsSecure Policy

L'impostazione del criterio TransformsSecure su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache locale nel computer dell'utente in un percorso in cui l'utente non ha accesso in scrittura. L'impostazione di questo criterio corrisponde all'impostazione [della proprietà TRANSFORMSSECURE,](transformssecure.md) ad eccezione del fatto che l'ambito è diverso. L'impostazione dei criteri TransformsSecure si applica a tutti i pacchetti installati in un determinato computer. L'impostazione della proprietà TRANSFORMSSECURE si applica al pacchetto indipendentemente dal computer.

Lo scopo di questo criterio è fornire un'archiviazione sicura delle trasformazioni con utenti in viaggio di Windows 2000. A partire Windows Server 2003, il valore predefinito di questo criterio è 1.

Quando questo criterio è impostato, [un'installazione di manutenzione](maintenance-installation.md) può usare solo la trasformazione dalla cache protetta. Nel caso in cui il programma di installazione ritieni che la trasformazione non è presente nel computer locale, il programma di installazione tenta di ripristinare la trasformazione. Per consentire al programma di installazione di ripristinare la trasformazione, la trasformazione protetta deve risiedere in un'origine autorizzata nell'elenco di origine del pacchetto di installazione. Per altre informazioni, vedere [Resilienza dell'origine.](source-resiliency.md) L'installazione di manutenzione non riesce se la trasformazione non è disponibile o non può essere caricata.

In Windows Server 2003, se questo criterio non è impostato, il comportamento predefinito è archiviare le trasformazioni in una posizione sicura. In tutte le versioni precedenti Windows Server 2003, se i criteri non sono impostati, il comportamento predefinito è archiviare le trasformazioni nel profilo degli utenti.

Per altre [informazioni, vedere](secured-transforms.md) anche Trasformazioni protette.

Windows Il programma di installazione [interpreta i criteri TransformsAtSource](transformsatsource-policy.md) in modo che siano uguali ai criteri TransformsSecure.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del computer** \\  \\ **locale** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



