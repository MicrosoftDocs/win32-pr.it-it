---
title: COM, DCOM e librerie dei tipi
description: Component Object Model (COM) e DCOM (Distributed Component Object Model) usano RPC (Remote Procedure Call) per consentire agli oggetti componente distribuito di comunicare tra loro.
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- interfacce MIDL , COM
- interfacce MIDL , DCOM
- interfacce MIDL, librerie dei tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997d2a61fef3e2bc46f4539dca2ecd67d8de385d402e5e9c862b267b697b3cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991761"
---
# <a name="com-dcom-and-type-libraries"></a>COM, DCOM e librerie dei tipi

Component Object Model (COM) e DCOM (Distributed Component Object Model) usano RPC (Remote Procedure Call) per consentire agli oggetti componente distribuito di comunicare tra loro. Pertanto, un'interfaccia COM o DCOM definisce l'identità e le caratteristiche esterne di un oggetto COM. Costituisce i mezzi con cui i client possono accedere ai metodi e ai dati di un oggetto. Con DCOM, questo accesso è possibile indipendentemente dal fatto che gli oggetti esistano nello stesso processo, processi diversi nello stesso computer o in computer diversi. Come per le interfacce client/server RPC, un oggetto COM o DCOM può esporre la funzionalità in diversi modi e tramite più interfacce.

## <a name="type-library"></a>Libreria dei tipi

Una libreria dei tipi (TLB) è un file binario che archivia le informazioni sulle proprietà e i metodi di un oggetto COM o DCOM in un modulo accessibile ad altre applicazioni in fase di esecuzione. Usando una libreria dei tipi, un'applicazione o un browser può determinare le interfacce supportate da un oggetto e richiamare i metodi di interfaccia di un oggetto. Ciò può verificarsi anche se le applicazioni client e dell'oggetto sono state scritte in linguaggi di programmazione diversi. L'ambiente di runtime COM/DCOM può anche usare una libreria dei tipi per fornire il marshalling automatico tra apartment, tra processi e tra computer per le interfacce descritte nelle librerie dei tipi.

## <a name="characteristics-of-an-interface"></a>Caratteristiche di un'interfaccia

Definire le caratteristiche di un'interfaccia in un file di definizione dell'interfaccia (IDL) e in un file di configurazione dell'applicazione (ACF) facoltativo:

-   Il file IDL specifica le caratteristiche delle interfacce dell'applicazione in transito, ovvero la modalità di trasmissione dei dati tra client e server o tra oggetti COM.
-   Il file ACF specifica le caratteristiche dell'interfaccia, ad esempio gli handle di associazione, che riguardano solo l'ambiente operativo locale. Il file ACF può anche specificare come effettuare il marshalling e trasmettere una struttura di dati complessa in un formato indipendente dal computer.

Per altre informazioni sui file IDL e ACF, vedere [File IDL e ACF.](/windows/desktop/Rpc/the-idl-and-acf-files)

I file IDL e ACF sono script scritti in Microsoft Interface Definition Language (MIDL), ovvero l'implementazione e l'estensione Microsoft del linguaggio IDL (Interface Definition Language) OSF-DCE. Le estensioni Microsoft per il linguaggio IDL consentono di creare interfacce COM e librerie dei tipi. Il compilatore, Midl.exe, usa questi script per generare stub in linguaggio C e file di intestazione, nonché file di libreria dei tipi.

## <a name="the-midl-compiler"></a>Compilatore MIDL

A seconda del contenuto del file IDL, il compilatore MIDL genererà uno dei file seguenti.

Un file proxy/stub in linguaggio C, un file di identificatore di interfaccia, un file di dati DLL e un file di intestazione correlato per un'interfaccia COM personalizzata. Il compilatore MIDL genera questi file quando rileva l'attributo dell'oggetto in un elenco di attributi dell'interfaccia. Per informazioni più dettagliate su questi file, vedere [File generati per un'interfaccia COM.](files-generated-for-a-com-interface.md)

Un file di libreria dei tipi compilato (con estensione tlb) e un file di intestazione correlato. MIDL genera questi file quando rileva [**un'istruzione library**](library.md) nel file IDL. Per informazioni generali sulle librerie dei tipi, vedere [Contenuto di una libreria dei tipi](/previous-versions/windows/desktop/automat/contents-of-a-type-library)in Guida di riferimento per programmatori di automazione.

File stub client e server in linguaggio C/C++ e file di intestazione correlato per un'interfaccia RPC. Questi file vengono generati quando nel file IDL sono presenti interfacce che non hanno [**l'attributo object.**](object.md) Per una panoramica dei file stub e di intestazione, vedere [Procedura di compilazione generale.](/windows/desktop/Rpc/general-build-procedure) Per informazioni più dettagliate, vedere [File generati per un'interfaccia RPC.](files-generated-for-an-rpc-interface.md)

 

 