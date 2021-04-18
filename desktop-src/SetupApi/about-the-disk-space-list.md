---
description: L'elenco spazio su disco consente di calcolare lo spazio su disco necessario per completare le operazioni di installazione.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Informazioni sull'elenco di Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306520"
---
# <a name="about-the-disk-space-list"></a>Informazioni sull'elenco di Disk-Space

L'elenco spazio su disco consente di calcolare lo spazio su disco necessario per completare le operazioni di installazione. Dopo aver creato un elenco di spazio su disco e aggiunto le operazioni su file, è possibile eseguire una query sull'elenco per determinare le unità di destinazione specificate dalle operazioni sui file e lo spazio su disco necessario in ogni unità.

Confrontando lo spazio necessario per lo spazio disponibile nei dischi di destinazione, è possibile determinare a livello di codice se è disponibile spazio sufficiente per l'installazione corrente.

È possibile aggiungere o rimuovere operazioni sui file nell'elenco spazio su disco e ricalcolare lo spazio su disco necessario. Questa funzionalità consente, ad esempio, di scrivere un programma che interagisce con l'utente, consentendo di scegliere i componenti che desiderano installare in base allo spazio su disco necessario.

Le funzioni elenco spazio su disco controllano automaticamente le copie dei file preesistenti nel disco di destinazione. Se viene rilevata una versione precedente del file, le funzioni elenco spazio su disco calcolano lo spazio aggiuntivo necessario per completare le operazioni sui file.

Se, ad esempio, un'operazione di copia specifica che un file a 6000 byte deve essere copiato nell'unità C e la versione 2000 byte di tale file esiste già nell'unità C, le funzioni di spazio su disco restituiranno uno spazio obbligatorio di 4000 byte. Lo spazio aggiuntivo viene usato per sostituire la versione precedente del file con la versione più recente.

L'elenco spazio su disco consente di eseguire il rounding dei file di dimensioni ai limiti del cluster di dischi.

 

 



