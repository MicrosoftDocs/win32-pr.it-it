---
title: Interfacce di servizio Active Directory
description: Introduzione alle interfacce di Active Directory Services, con collegamenti a diverse guide.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfacce del servizio Active Directory (vedere ADSI)
- ADSI ADSI, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047359"
---
# <a name="active-directory-service-interfaces"></a>Interfacce di servizio Active Directory

## <a name="purpose"></a>Scopo

Active Directory Service Interfaces (ADSI) è un set di interfacce COM utilizzate per accedere alle funzionalità dei servizi directory da provider di rete diversi. ADSI viene utilizzato in un ambiente di elaborazione distribuita per presentare un unico set di interfacce del servizio directory per la gestione delle risorse di rete. Gli amministratori e gli sviluppatori possono utilizzare i servizi ADSI per enumerare e gestire le risorse in un servizio directory, indipendentemente dall'ambiente di rete che contiene la risorsa.

ADSI consente attività amministrative comuni, ad esempio l'aggiunta di nuovi utenti, la gestione delle stampanti e l'individuazione delle risorse in un ambiente di elaborazione distribuito.

> [!Note]  
> La documentazione seguente è destinata ai programmatori di computer. Se si è un utente finale che tenta di eseguire il debug di un errore di stampa o di una rete domestica, vedere i [Forum della community Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Se applicabile

Gli amministratori di rete possono utilizzare ADSI per automatizzare le attività comuni, ad esempio l'aggiunta di utenti e gruppi, la gestione delle stampanti e l'impostazione delle autorizzazioni per le risorse di rete.

I fornitori di software indipendenti e gli sviluppatori di utenti finali possono utilizzare ADSI per "abilitare la directory" dei propri prodotti e applicazioni. I servizi possono essere pubblicati in una directory, i client possono utilizzare la directory per trovare i servizi ed entrambi possono utilizzare la directory per individuare e modificare altri oggetti di interesse. Poiché le interfacce del servizio Active Directory sono indipendenti dai servizi directory sottostanti, i prodotti e le applicazioni abilitati alla directory possono funzionare correttamente in più ambienti di rete e di directory.

## <a name="developer-audience"></a>Sviluppatori

È possibile scrivere applicazioni client ADSI in molte lingue. Per la maggior parte delle attività amministrative, ADSI definisce le interfacce e gli oggetti accessibili da linguaggi conformi all'automazione come Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) e Java ai linguaggi più performanti e in efficienza, ad esempio C e C++. Una valida base nella programmazione COM è utile per il programmatore ADSI.

## <a name="run-time-requirements"></a>Requisiti di runtime

Active Directory viene eseguito nei controller di dominio di Windows Server. Tuttavia, le applicazioni client che utilizzano ADSI possono essere scritte ed eseguite in Windows. Inoltre, gli sviluppatori vorranno la piattaforma Software Development Kit (SDK), disponibile anche nel sito Web MSDN. Per esaminare il contenuto di Active Directory, utilizzare lo snap-in MMC utenti e computer Active Directory. Questo snap-in sostituisce lo strumento ADSVW disponibile per le versioni precedenti di Windows.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Informazioni su ADSI](about-adsi.md)
</dt> <dd>

Informazioni generali su ADSI.

</dd> <dt>

[Uso di ADSI](using-adsi.md)
</dt> <dd>

Guida per programmatori per l'utilizzo di ADSI.

</dd> <dt>

[Esercitazioni introduttive di ADSI](adsi-quick-start-tutorials.md)
</dt> <dd>

Uso di ADSI con automazione per la gestione delle directory.

</dd> <dt>

[Riferimenti ADSI](adsi-reference.md)
</dt> <dd>

Documentazione di interfacce e metodi ADSI.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Component Object Model (COM)](../com/the-component-object-model.md)
</dt> <dt>

[Client e server COM](../com/com-clients-and-servers.md)
</dt> <dt>

[Active Directory Domain Services](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 