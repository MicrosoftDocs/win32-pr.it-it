---
description: Gli autori di pacchetti devono assicurarsi che i nomi delle tabelle, delle proprietà o delle azioni personalizzate definite nel pacchetto non siano in conflitto con i nomi delle tabelle, delle proprietà o delle azioni standard native per la Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Denominazione di tabelle, proprietà e azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880726"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Denominazione di tabelle, proprietà e azioni personalizzate

Gli autori di pacchetti devono assicurarsi che i nomi delle tabelle, delle proprietà o delle azioni personalizzate definite nel pacchetto non siano in conflitto con i nomi delle tabelle, delle proprietà o delle azioni standard native per la Windows Installer.

Gli autori dei pacchetti devono rispettare le linee guida seguenti per i nomi di tabelle, proprietà o azioni personalizzati.

-   Creare nomi per le tabelle, le proprietà o le azioni personalizzate con prefisso che identifica l'applicazione.
-   Non usare mai un nome con MSI come prefisso. A partire da Windows Installer 2,0, a tutte le nuove proprietà, azioni e tabelle native Windows Installer sono assegnati nomi con prefisso MSI. Questo prefisso non distingue tra maiuscole e minuscole, ad esempio MsiNewInternalTable. Poiché il prefisso non distingue tra maiuscole e minuscole, gli autori devono evitare tutti i case del prefisso MSI.

Per ulteriori informazioni, vedere [nomi di tabella](table-names.md).

 

 



