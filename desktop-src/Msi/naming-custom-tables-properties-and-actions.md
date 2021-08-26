---
description: Gli autori di pacchetti devono assicurarsi che i nomi delle tabelle, delle proprietà o delle azioni personalizzate definite nel pacchetto non siano in conflitto con i nomi delle tabelle standard, delle proprietà o delle azioni native del programma di installazione Windows.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Denominazione di tabelle, proprietà e azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd26ab08bcada936bdcb9c87d10cb060c697689cec8978a1eae0d25ac5c0a2d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105081"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Denominazione di tabelle, proprietà e azioni personalizzate

Gli autori di pacchetti devono assicurarsi che i nomi delle tabelle, delle proprietà o delle azioni personalizzate definite nel pacchetto non siano in conflitto con i nomi delle tabelle standard, delle proprietà o delle azioni native del programma di installazione Windows.

Gli autori di pacchetti devono rispettare le linee guida seguenti per i nomi di tabelle, proprietà o azioni personalizzati.

-   Creare nomi per tabelle, proprietà o azioni personalizzate con un prefisso che identifica l'applicazione.
-   Non usare mai un nome con Msi come prefisso. A partire da Windows Installer 2.0, a tutte le nuove proprietà, azioni e tabelle del programma di installazione Windows nativo vengono specificati nomi con prefisso Msi. Questo prefisso non fa distinzione tra maiuscole e minuscole, ad esempio MsiNewInternalTable. Poiché il prefisso non fa distinzione tra maiuscole e minuscole, gli autori devono evitare tutti i casi del prefisso Msi.

Per altre informazioni, vedere [Nomi di tabella](table-names.md).

 

 



