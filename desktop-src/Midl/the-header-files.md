---
title: File di intestazione
description: Il file di intestazione dell'interfaccia (Name.h) contiene definizioni di tipo e dichiarazioni di funzione basate sulla definizione dell'interfaccia nel file IDL corrente, nonché tutti i tipi di dati e le operazioni dichiarate nei file inclusi nella direttiva \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- file di intestazione MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac9bc5e8b5edd091450af670fd51d251326029f13e1f88a6d5a9116faa5b4447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013519"
---
# <a name="the-header-files"></a>File di intestazione

Il file di intestazione dell'interfaccia (Name.h) contiene definizioni di tipo e dichiarazioni di funzione basate sulla definizione dell'interfaccia nel file IDL corrente, nonché tutti i tipi di dati e le operazioni dichiarati nei file inclusi nella direttiva \# include. I tipi di dati dei file importati con la direttiva import non vengono replicati nel file di intestazione. al contrario, il file di intestazione generato contiene una riga di inclusione per il file H generato dal file importato.

Includere questo file nei file di origine per la DLL proxy e per le applicazioni client che usano l'interfaccia .

Il nome predefinito per un file di intestazione generato da un file.idl è File.h. [**L'opzione del compilatore**](-header.md) MIDL /header esegue l'override del nome predefinito del file di intestazione dell'interfaccia.

 

 




