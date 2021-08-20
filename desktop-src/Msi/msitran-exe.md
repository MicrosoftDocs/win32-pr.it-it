---
description: Msitran.exe usa MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo e MsiDatabaseApplyTransform per generare o applicare un file di trasformazione. Questo strumento è disponibile solo nei componenti dell'SDK Windows per Windows programma di installazione.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09803623024bb593897411a5e852aa953335c31fd88f9e2e1922b89b53e9abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944269"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe usa [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)e [**MsiDatabaseApplyTransform per**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) generare o applicare un file di trasformazione.

Questo strumento è disponibile solo in componenti Windows [SDK per sviluppatori Windows Programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintassi

Usare la sintassi seguente per generare una trasformazione.

**msitran -g** *{base db}{ref db}{nome file di trasformazione} \[ {condizioni di errore/condizioni di convalida} \]*

Usare la sintassi seguente per applicare una trasformazione

**msitran -a** *{transform}{database} \[ {condizioni di errore} \]*

## <a name="command-line-options"></a>Opzioni da riga di comando

Msitran.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole. È anche possibile usare un delimitatore barra al posto di un trattino.



| Opzione | Descrizione            |
|--------|------------------------|
| -g     | Generazione di trasformazioni.  |
| -a     | Trasformare l'applicazione. |



 

Gli errori seguenti possono essere eliminati quando si applica una trasformazione. Per eliminare un errore, includere il carattere appropriato nell'argomento {condizioni di errore}. Le condizioni specificate con -g vengono inserite nelle informazioni di riepilogo della trasformazione, ma non vengono usate quando si applica una trasformazione con -a. Per informazioni, vedere [**MsiDatabaseApplyTransform.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)



| Opzione | Errore eliminato           |
|--------|----------------------------|
| a      | Aggiungere una riga esistente.          |
| b      | Eliminare una riga non esistente.   |
| c      | Aggiungere una tabella esistente.        |
| d      | Eliminare una tabella non esistente. |
| h      | Modificare la riga esistente.       |
| f      | Modificare la tabella codici.           |



 

Le condizioni di convalida seguenti possono essere utilizzate per indicare quando una trasformazione può essere applicata a un pacchetto. Queste condizioni possono essere specificate con -g, ma non con -a.



| Opzione | Condizione di convalida                                  |
|--------|-------------------------------------------------------|
| g      | Controllare il codice di aggiornamento.                                   |
| l      | Controllare la lingua.                                       |
| p      | Controllare la piattaforma.                                       |
| r      | Controllare il prodotto.                                        |
| s      | Controllare solo la versione principale.                             |
| t      | Controllare solo le versioni principali e secondarie.                  |
| u      | Controllare le versioni principali, secondarie e di aggiornamento.             |
| v      | Versione del database applicata < di database di base.  |
| w      | Versione del database applicata <= versione del database di base. |
| x      | Versione del database applicata = versione di base del database.     |
| y      | Versione del database applicata >= versione del database di base. |
| z      | Versione del database applicata > di database di base.  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Trasformazioni di database](database-transforms.md)
</dt> <dt>

[Esempio di trasformazione di personalizzazione](a-customization-transform-example.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



