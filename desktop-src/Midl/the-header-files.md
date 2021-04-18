---
title: File di intestazione
description: Il file di intestazione dell'interfaccia (Name. h) contiene le definizioni di tipo e le dichiarazioni di funzione basate sulla definizione dell'interfaccia nel file IDL corrente, nonché su tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la direttiva \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- file di intestazione MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298627"
---
# <a name="the-header-files"></a>File di intestazione

Il file di intestazione dell'interfaccia (Name. h) contiene le definizioni di tipo e le dichiarazioni di funzione basate sulla definizione dell'interfaccia nel file IDL corrente, nonché su tutti i tipi di dati e le operazioni dichiarati nei file inclusi con la \# direttiva include. I tipi di dati dei file importati con la direttiva Import non vengono replicati nel file di intestazione. il file di intestazione generato contiene invece una riga di inclusione per il file H generato dal file importato.

Includere questo file nei file di origine per la DLL del proxy e per le applicazioni client che utilizzano l'interfaccia.

Il nome predefinito per un file di intestazione generato da un file. idl è file. h. L'opzione del compilatore MIDL [**/header**](-header.md) esegue l'override del nome predefinito del file di intestazione dell'interfaccia.

 

 




