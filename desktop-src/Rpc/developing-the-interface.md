---
title: Sviluppo dell'interfaccia
description: Un'interfaccia RPC descrive le funzioni remote implementate dal programma server.
ms.assetid: f0dfe9d1-fe84-461c-8684-147fbd0bdefe
keywords:
- RPC (Remote Procedure Call), attività, sviluppo dell'interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b6f720bcd492e784ad07fe20e221ac54951680
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118210"
---
# <a name="developing-the-interface"></a>Sviluppo dell'interfaccia

Un'interfaccia RPC descrive le funzioni remote implementate dal programma server. L'interfaccia garantisce che il client e il server comunicano utilizzando le stesse regole quando il client richiama una procedura remota offerta dal server. Un'interfaccia è costituita da un nome di interfaccia, da alcuni attributi, da definizioni di costanti o di tipi facoltativi e da un set di dichiarazioni di routine. Ogni dichiarazione di routine deve contenere un nome di routine, un tipo restituito e un elenco di parametri.

Le interfacce sono definite nel Microsoft Interface Definition Language (MIDL). Se si ha familiarità con C o C++, le definizioni dell'interfaccia MIDL sembrano piuttosto semplici. MIDL è simile a C e C++ in molti modi.

Quando si sviluppa un'applicazione RPC, viene utilizzato un editor di testo per definire l'interfaccia e archiviarla in un file di testo con estensione IDL. Per ulteriori informazioni, vedere [i file IDL e ACF](the-idl-and-acf-files.md). Il compilatore MIDL genera un file di intestazione che il programma include nei file di origine client e server. Il compilatore MIDL genera anche due file di origine C. È possibile compilare e collegare uno di questi al programma client e l'altro al programma server. Questi due file di origine C sono gli stub client e server. Per una panoramica degli stub client e server, vedere funzionamento di [RPC](how-rpc-works.md). Per una panoramica sul compilatore MIDL, vedere [compilazione di un file MIDL](using-midl.md).

Per impostazione predefinita, lo stub del client e del server ha lo stesso nome, che può causare problemi se il client si collega con lo stub del server o viceversa. L'uso dell'opzione MIDL [**/Prefix**](/windows/desktop/Midl/-prefix) impedisce che si verifichi questo errore comune.

Nella figura seguente viene illustrato il processo di creazione di un'interfaccia.

![la creazione di stub client e server con l'opzione/prefix impedisce problemi di compilazione accidentale](images/idldev.png)

È anche possibile che sia necessario specificare un file di configurazione dell'applicazione (ACF) per l'input anche per il compilatore MIDL. Per ulteriori informazioni sui file di configurazione dell'applicazione, vedere [i file IDL e ACF](the-idl-and-acf-files.md).

Oltre al compilatore MIDL, in genere è necessario usare l'utilità uuidgen per generare un identificatore univoco universale (UUID, interscambiabile con il termine GUID). In questa sezione vengono presentate informazioni su entrambi gli strumenti, divisi negli argomenti seguenti:

-   [Generazione UUID dell'interfaccia](generating-interface-uuids.md)
-   [Uso di MIDL](using-midl.md)

 

 