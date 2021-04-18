---
description: Msitran.exe USA MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo e MsiDatabaseApplyTransform per generare o applicare un file di trasformazione. Questo strumento è disponibile solo nei componenti Windows SDK per Windows Installer sviluppatori.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316257"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe USA [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)e [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) per generare o applicare un file di trasformazione.

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintassi

Utilizzare la sintassi seguente per generare una trasformazione.

**MSITran-g** *{base DB} {Ref DB} {nome file di trasformazione} \[ {condizioni di errore/condizioni \] di convalida}*

Utilizzare la sintassi seguente per applicare una trasformazione

**MSITran-a** *{Transform} {database} \[ {condizioni di errore \] }*

## <a name="command-line-options"></a>Opzioni da riga di comando

Msitran.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.



| Opzione | Descrizione            |
|--------|------------------------|
| -g     | Generazione della trasformazione.  |
| -a     | Trasforma applicazione. |



 

Quando si applica una trasformazione, è possibile che vengano eliminati gli errori seguenti. Per non visualizzare un errore, includere il carattere appropriato nell'argomento {error conditions}. Le condizioni specificate con-g vengono inserite nelle informazioni di riepilogo della trasformazione, ma non vengono utilizzate quando si applica una trasformazione con-a. Per informazioni, vedere [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).



| Opzione | Errore eliminato           |
|--------|----------------------------|
| a      | Aggiungi riga esistente.          |
| b      | Elimina la riga non esistente.   |
| c      | Aggiungere una tabella esistente.        |
| d      | Elimina la tabella non esistente. |
| h      | Modificare la riga esistente.       |
| f      | Modificare la tabella codici.           |



 

Le condizioni di convalida seguenti possono essere utilizzate per indicare quando una trasformazione può essere applicata a un pacchetto. Queste condizioni possono essere specificate con-g, ma non con-a.



| Opzione | Condizione di convalida                                  |
|--------|-------------------------------------------------------|
| g      | Controllare il codice di aggiornamento.                                   |
| l      | Controllare la lingua.                                       |
| p      | Controllare la piattaforma.                                       |
| r      | Verificare il prodotto.                                        |
| s      | Controllare solo la versione principale.                             |
| u      | Controllare solo le versioni principale e secondaria.                  |
| u      | Controllare le versioni principale, secondaria e di aggiornamento.             |
| v      | Versione del database applicata < versione del database di base.  |
| w      | Versione del database applicata <= versione del database di base. |
| x      | Versione del database applicata = versione del database di base.     |
| y      | Versione del database applicata >= versione del database di base. |
| z      | Versione del database applicata > versione del database di base.  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Trasformazioni di database](database-transforms.md)
</dt> <dt>

[Esempio di trasformazione della personalizzazione](a-customization-transform-example.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



