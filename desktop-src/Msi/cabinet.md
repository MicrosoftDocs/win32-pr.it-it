---
description: Il tipo di dati Cab deve essere utilizzato nella colonna Cab della tabella Supporti .
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: armadietto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16acfd031a6580f898d4cb464a15c895644995a2499a62ac79c9adeced8ccec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105361"
---
# <a name="cabinet"></a>armadietto

Il tipo di dati Cab deve essere usato nella colonna Cabinet della [tabella Media](media-table.md).

Se il nome dell'archivio è preceduto dal simbolo di numero, il file CAB viene archiviato come flusso di dati all'interno del pacchetto. La stringa di caratteri che segue \# è un identificatore [per](identifier.md) questo flusso di dati. Si noti che se il file CAB viene archiviato come flusso di dati, il nome di un file CAB fa distinzione tra maiuscole e minuscole.

Se il nome dell'archivio non è preceduto dal simbolo di numero , il file CAB viene archiviato in un file separato che si trova nella radice dell'albero di origine specificato dalla \# [tabella di directory](directory-table.md). Il file CAB deve usare la sintassi del nome file breve costituita da un nome di otto caratteri, un punto e un'estensione di tre caratteri. Il tipo di dati Cab non può usare la \| sintassi short longname per i nomi di file. Se il file CAB viene archiviato come file separato, il nome del file CAB non fa distinzione tra maiuscole e minuscole.

Per risparmiare spazio su disco, il programma di installazione rimuove tutti i file CAB incorporati nel file .msi prima di memorizzare nella cache il pacchetto di installazione nel computer dell'utente.

Vedere [Inclusione di un file CAB in un'installazione](including-a-cabinet-file-in-an-installation.md)di .

 

 



