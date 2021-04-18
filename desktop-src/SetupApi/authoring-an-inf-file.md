---
description: Quando si crea un file INF per un'applicazione di installazione, è necessario fare riferimento anche al formato di file INF descritto in linee guida generali per i file INF e le sezioni e le direttive del file inf del Microsoft Windows 2000 Driver Development Kit.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Creazione di un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306514"
---
# <a name="authoring-an-inf-file"></a>Creazione di un file INF

Quando si crea un file INF per un'applicazione di installazione, è necessario fare riferimento anche al formato di file INF descritto in *linee guida generali per i file inf* e le *sezioni e le direttive del file* inf del Microsoft Windows 2000 Driver Development Kit.

Quando si creano file INF per un'applicazione di installazione, attenersi alle regole seguenti.

-   Una sezione **Version** è obbligatoria in ogni file inf.
-   Le sezioni devono iniziare con il nome della sezione racchiuso tra parentesi quadre ( \[ \] ).
-   I nomi delle sezioni **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** e **Version** devono essere identici a quelli del tipo di sezione. Ad esempio \[ , usare DestinationDirs \] . Gli autori possono specificare i nomi di altri tipi di sezioni.
-   I nomi delle sezioni **SourceDisksNames** e **SourceDisksFiles** possono essere aggiunti con un suffisso specifico della piattaforma. Per visualizzare, ad esempio, una sezione **SourceDisksNames** specifica di Intel, utilizzare \[ SourceDisksNames. x86 \] . Se le funzioni di installazione trovano sezioni specifiche della piattaforma **SourceDisksNames** e **SourceDisksFiles** che corrispondono alla piattaforma dell'utente, le funzioni usano le sezioni specifiche della piattaforma. In caso contrario, le funzioni di installazione utilizzano le sezioni **SourceDisksNames** e **SourceDisksFiles** senza suffisso. Le funzioni di installazione possono determinare a livello di codice il sistema dell'utente. Vedere l' [esempio di sezioni inf SourceDisksNames e SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).
-   I valori possono essere espressi come stringhe sostituibili utilizzando il formato%*strKey*%. Per usare un carattere% nella stringa, usare%%. StrKey deve essere definito in una sezione **Strings** del file inf.

 

 



