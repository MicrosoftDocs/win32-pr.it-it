---
title: Librerie di tipi COM, DCOM e
description: Component Object Model (COM) e Distributed Component Object Model (DCOM) utilizzano Remote Procedure Call (RPC) per consentire agli oggetti componente distribuiti di comunicare tra loro.
ms.assetid: 7bade397-676e-43be-82f4-b23cd768fd16
keywords:
- interfacce MIDL, COM
- interfacce MIDL, DCOM
- interfacce MIDL, librerie di tipi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f0b21aad9f88f02d8029d478eead50f5501ecc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872449"
---
# <a name="com-dcom-and-type-libraries"></a>Librerie di tipi COM, DCOM e

Component Object Model (COM) e Distributed Component Object Model (DCOM) utilizzano Remote Procedure Call (RPC) per consentire agli oggetti componente distribuiti di comunicare tra loro. Pertanto, un'interfaccia COM o DCOM definisce l'identità e le caratteristiche esterne di un oggetto COM. Costituisce i mezzi mediante i quali i client possono accedere ai metodi e ai dati di un oggetto. Con DCOM, questo accesso è possibile, indipendentemente dal fatto che gli oggetti esistano nello stesso processo, processi diversi nello stesso computer o in computer diversi. Come per le interfacce client/server RPC, un oggetto COM o DCOM può esporre le proprie funzionalità in diversi modi e tramite più interfacce.

## <a name="type-library"></a>Libreria di tipi

Una libreria dei tipi (con estensione tlb) è un file binario che archivia le informazioni relative alle proprietà e ai metodi di un oggetto COM o DCOM in un modulo accessibile ad altre applicazioni in fase di esecuzione. Utilizzando una libreria dei tipi, un'applicazione o un browser può determinare quali interfacce sono supportate da un oggetto e richiamare i metodi di interfaccia di un oggetto. Questa situazione può verificarsi anche se l'oggetto e le applicazioni client sono stati scritti in linguaggi di programmazione diversi. L'ambiente di runtime COM/DCOM può inoltre utilizzare una libreria dei tipi per fornire il marshalling automatico tra Apartment, cross-process e tra computer per le interfacce descritte nelle librerie dei tipi.

## <a name="characteristics-of-an-interface"></a>Caratteristiche di un'interfaccia

È possibile definire le caratteristiche di un'interfaccia in un file di definizione di interfaccia (IDL) e un file di configurazione dell'applicazione (ACF) facoltativo:

-   Il file IDL specifica le caratteristiche delle interfacce dell'applicazione in transito, ovvero la modalità di trasmissione dei dati tra client e server o tra oggetti COM.
-   Il file ACF specifica le caratteristiche dell'interfaccia, ad esempio gli handle di binding, che riguardano solo l'ambiente operativo locale. Il file ACF consente inoltre di specificare come effettuare il marshalling e trasmettere una struttura di dati complessa in un form indipendente dal computer.

Per ulteriori informazioni sui file IDL e ACF, vedere [i file IDL e ACF](/windows/desktop/Rpc/the-idl-and-acf-files).

I file IDL e ACF sono script scritti in Microsoft Interface Definition Language (MIDL), ovvero l'implementazione Microsoft e l'estensione di OSF-DCE Interface Definition Language (IDL). Le estensioni Microsoft per il linguaggio IDL consentono di creare interfacce COM e librerie dei tipi. Il compilatore, Midl.exe, usa questi script per generare stub e file di intestazione del linguaggio C, nonché file di libreria dei tipi.

## <a name="the-midl-compiler"></a>Compilatore MIDL

A seconda del contenuto del file IDL, il compilatore MIDL genererà uno dei file seguenti.

Un file di proxy/stub in linguaggio C, un file di identificatore di interfaccia, un file di dati DLL e un file di intestazione correlato per un'interfaccia COM personalizzata. Il compilatore MIDL genera questi file quando rileva l'attributo dell'oggetto in un elenco di attributi di interfaccia. Per informazioni più dettagliate su questi file, vedere [file generati per un'interfaccia com](files-generated-for-a-com-interface.md).

Un file di libreria di tipi compilato (con estensione tlb) e un file di intestazione correlato. MIDL genera questi file quando rileva un'istruzione di [**libreria**](library.md) nel file IDL. Per informazioni generali sulle librerie dei tipi, vedere il [contenuto di una libreria dei tipi](/previous-versions/windows/desktop/automat/contents-of-a-type-library)nella Guida di riferimento per programmatori di automazione.

File stub client e server in linguaggio C/C++ e file di intestazione correlato per un'interfaccia RPC. Questi file vengono generati quando nel file IDL sono presenti interfacce che non dispongono dell'attributo [**Object**](object.md) . Per una panoramica dei file di intestazione e dello stub, vedere [procedura generale di compilazione](/windows/desktop/Rpc/general-build-procedure). Per informazioni più dettagliate, vedere [file generati per un'interfaccia RPC](files-generated-for-an-rpc-interface.md).

 

 