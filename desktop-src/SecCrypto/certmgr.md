---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0e248aef1f726b16d8f17098cfc9642393b963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131438"
---
# <a name="certmgr"></a>CertMgr

Gli strumenti CertMgr sostituiscono DumpCert. Sono incluse nuove funzionalità per la gestione di [*certificati*](../secgloss/c-gly.md), [*elenchi di certificati attendibili*](../secgloss/c-gly.md) (scopi consentiti) e [*elenchi di revoche di certificati*](../secgloss/c-gly.md) (CRL). Lo strumento viene installato nella \\ cartella bin del percorso di installazione di Microsoft Windows Software Development Kit (SDK).

CertMgr è disponibile come parte del Windows SDK, da cui è possibile scaricare <https://go.microsoft.com/fwlink/p/?linkid=84091> .

CertMgr esegue una delle quattro funzioni a seconda dell'azione indicata nel comando.

**Certmgr** \[ **-Aggiungi** \| **-Canc** \| **-put** \] \[  Opzioni \] di \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *Destination*\]

Nella tabella seguente sono indicate le azioni di base dello strumento CertMgr.



| Flag azione | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno        | Visualizza i certificati, i CRL o scopi consentiti. senza flag di azione (solo per la visualizzazione), *SourceName* è il nome dell'archivio certificati o del file contenente gli elementi da visualizzare. L'archivio può essere un archivio [*serializzato*](../secgloss/s-gly.md) (StoreFile) o un archivio di sistema. Per impostazione predefinita, CertMgr Visualizza tutti i certificati, scopi consentiti o CRL nell'archivio certificati o nel file. *Destination* non viene utilizzato per la visualizzazione.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -aggiungere        | Copia i certificati, scopi consentiti e CRL in un archivio certificati. Quando si usa **-Add**, *SourceName* è l'archivio certificati di origine che contiene i certificati esistenti, scopi consentiti e CRL. *Destination* è l'archivio certificati di destinazione a cui verranno aggiunti i certificati, scopi consentiti e CRL. L'archivio di destinazione verrà salvato come archivio [*serializzato*](../secgloss/s-gly.md) , a meno che non venga utilizzata l'opzione **-7** , che salva l'archivio come [](../secgloss/p-gly.md) \# file PKCS 7. Si noti che non è possibile usare l'opzione **-7** quando l'archivio di destinazione è un archivio di sistema.<br/>                                                                                                                          |
| -CANC        | Elimina i certificati, scopi consentiti e CRL da un archivio certificati. Quando si usa **-Canc**, *SourceName* è l'archivio certificati di origine che contiene i certificati esistenti, scopi consentiti e CRL. *Destination* è l'archivio certificati di destinazione che conterrà copie dei certificati rimanenti, scopi consentiti e CRL dopo l'eliminazione degli elementi specificati. Se *Destination* non è specificato, *SourceName* fungerà anche da archivio di destinazione, che verrà modificato. L'archivio di destinazione verrà salvato come archivio [*serializzato*](../secgloss/s-gly.md) , a meno che non venga utilizzata l'opzione **-7** , che salva l'archivio come \# file PKCS 7. Si noti che non è possibile usare l'opzione **-7** quando l'archivio di destinazione è un archivio di sistema.<br/> |
| -Put        | Salva un certificato con codifica [*X. 509*](../secgloss/x-gly.md) , un elenco di scopi consentiti o un CRL in un file. Quando si usa **-put**, *SourceName* è l'archivio certificati di origine che contiene i certificati esistenti, scopi consentiti e CRL. *Destination* è il nome di un file in cui verranno salvati un certificato [*X. 509*](../secgloss/x-gly.md) con codifica, CTL e CRL. Se si usa l'opzione **-7** , il file verrà salvato come \# file PKCS 7.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Opzioni

Le opzioni seguenti si applicano a tutte le funzioni CertMgr eccetto se indicato.



| Opzione                     | Flag azione                                 | Descrizione                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | Nessuno (solo visualizzazione)                         | Modalità dettagliata. Visualizza informazioni dettagliate su certificati, scopi consentiti e CRL. Per impostazione predefinita, vengono visualizzate brevi informazioni.                                                                                                                       |
| **-c**                     | all                                         | Usare solo i certificati.                                                                                                                                                                                                                             |
| **-CTL**                   | all                                         | Usare solo scopi consentiti.                                                                                                                                                                                                                                     |
| **-CRL**                   | all                                         | USA solo CRL.                                                                                                                                                                                                                                     |
| **-tutto**                   | **-Add-CANC**<br/> **-Put**<br/> | Aggiunge tutte le voci del tipo scelto.                                                                                                                                                                                                               |
| **-e** *EncodingType*      | all                                         | [*Tipo di codifica*](../secgloss/e-gly.md)del certificato.                                                                                                                                             |
| **-y** *storeProviderType* | all                                         | Tipo di provider dell'archivio.                                                                                                                                                                                                                               |
| **-7**                     | **-Add-CANC**<br/> **-Put**<br/> | Salva l'archivio di destinazione come \# file PKCS 7.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | all                                         | Flag di apertura archivio. Si tratta del parametro *dwFlags* passato a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore). Il valore predefinito è CERT \_ System \_ Store \_ Current \_ User. Significativo solo se è impostato **-y** . Per ulteriori informazioni, vedere **CertOpenStore**.         |
| **-n** *commonNameString*  | **-Add-CANC**<br/> **-Put**<br/> | Nome comune del certificato. Può essere utilizzato solo con i certificati.                                                                                                                                                                                |
| **-SHA1** *SHA1Hash*       | **-Add-CANC**<br/> **-Put**<br/> | Hash SHA1 del certificato, dell'elenco di scopi consentiti o del CRL da copiare, eliminare o salvare.                                                                                                                                                                         |
| **-s**                     | all                                         | Indica che l'archivio è un archivio di sistema.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | all                                         | Percorso del registro di sistema dell'archivio certificati di sistema. Significativo solo quando è impostato **-s** . Deve essere impostato su *CurrentUser* (chiave del registro di sistema HKEY \_ Current \_ User) o *LocalMachine* (chiave del registro di sistema HKEY \_ Local \_ computer). *CurrentUser* è il valore predefinito. |
| **-?**                     | all                                         | Consente di visualizzare tutte le opzioni.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

CertMgr è supportato solo in Internet Explorer 4,0 o versione successiva.

CertMgr può copiare, eliminare o salvare uno o più certificati, scopi consentiti o CRL. Se è presente più di un elemento in una di queste categorie, l'utente dispone di tre opzioni:

-   Usare l'opzione **-All** per copiare, eliminare o salvare tutti gli elementi nella categoria indicata.
-   Usare le opzioni **-n** e **-SHA1** per identificare in modo univoco l'elemento da copiare, eliminare o salvare.
-   Se **-All** o **-n** e **-SHA1** non sono indicati, certmgr chiede all'utente un elenco di elementi da copiare, eliminare o salvare. L'utente risponde immettendo l'indice dell'elemento da copiare, eliminare o salvare.

Le azioni di CertMgr utilizzano variazioni minime della sintassi e delle opzioni. È necessario utilizzare la sintassi e le opzioni specifiche di un'azione.

CertMgr funziona con due tipi di archivi certificati: StoreFile e archivio di sistema. Un StoreFile può essere uno dei seguenti tipi di file:

-   Un file CTL/CRL/Certificate codificato (potrebbe essere codificato in base 64)
-   Un \# file PKCS 7
-   Documento firmato
-   StoreFile serializzato

Non è necessario specificare il tipo di StoreFile. CertMgr può determinare il tipo StoreFile ed eseguire le azioni appropriate.

Un archivio di sistema è un archivio certificati che si trova in genere nel registro di sistema in **CurrentUser**. L'utente può fare riferimento a un archivio di sistema fornendo solo il nome. Non è necessario specificare il tipo di provider dell'archivio certificati. A seconda del tipo di StoreFile o dell'archivio di sistema, CertMgr sceglie il tipo di provider dell'archivio corrispondente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di CertMgr](using-certmgr.md)
</dt> </dl>

 

 
