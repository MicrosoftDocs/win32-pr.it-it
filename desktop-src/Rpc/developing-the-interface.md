---
title: Sviluppo dell'interfaccia
description: Un'interfaccia RPC descrive le funzioni remote implementate dal programma server.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- Chiamata di procedura remota RPC, attività, sviluppo dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23829dcf143f63e791984e51194686d193d69cd575fadbc0e29c13a6f2279df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930606"
---
# <a name="developing-the-interface"></a>Sviluppo dell'interfaccia

Un'interfaccia RPC descrive le funzioni remote implementate dal programma server. L'interfaccia garantisce che il client e il server comunichino usando le stesse regole quando il client richiama una procedura remota offerta dal server. Un'interfaccia è costituita da un nome di interfaccia, alcuni attributi, definizioni facoltative di tipi o costanti e un set di dichiarazioni di routine. Ogni dichiarazione di routine deve contenere un nome di routine, un tipo restituito e un elenco di parametri.

Le interfacce sono definite nella Microsoft Interface Definition Language (MIDL). Se si ha familiarità con C o C++, le definizioni di interfaccia MIDL saranno piuttosto semplici. MIDL è simile a C e C++ in molti modi.

Quando si sviluppa un'applicazione RPC, viene usato un editor di testo per definire l'interfaccia e archiviarla in un file di testo con estensione idl. Per altre informazioni, vedere [File IDL e ACF](the-idl-and-acf-files.md). Il compilatore MIDL genera un file di intestazione che il programma include nei file di origine client e server. Il compilatore MIDL genera anche due file di origine C. Uno di questi viene compilato e collegato al programma client e l'altro al programma server. Questi due file di origine C sono gli stub client e server. Per una panoramica degli stub client e server, vedere [Funzionamento di RPC](how-rpc-works.md). Per una panoramica del compilatore MIDL, vedere [Compilazione di un file MIDL](using-midl.md).

Per impostazione predefinita, lo stub client e server hanno lo stesso nome, che può causare problemi se il client si collega allo stub del server o viceversa. L'uso [**dell'opzione MIDL /prefix**](/windows/desktop/Midl/-prefix) impedisce che si verifichi questo errore comune.

La figura seguente illustra il processo di creazione di un'interfaccia.

![la creazione di stub client e server con l'opzione /prefix impedisce problemi di compilazione accidentali](images/idldev.png)

È anche possibile che sia necessario specificare un file di configurazione dell'applicazione (ACF) per l'input anche per il compilatore MIDL. Per altre informazioni sui file di configurazione dell'applicazione, vedere [File IDL e ACF](the-idl-and-acf-files.md).

Oltre al compilatore MIDL, in genere è necessario usare l'utilità Uuidgen per generare un identificatore univoco universale (UUID, Universal Unique Identifier, intercambiabile con il termine GUID). Questa sezione presenta informazioni su entrambi questi strumenti, suddivisi negli argomenti seguenti:

-   [Generazione di UUID dell'interfaccia](generating-interface-uuids.md)
-   [Uso di MIDL](using-midl.md)

 

 