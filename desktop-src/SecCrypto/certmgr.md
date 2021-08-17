---
description: CertMgr
ms.assetid: c9b68a81-c4f7-4754-9b47-c83f3679f0e3
title: CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832610510eeb74b821ec690cab93fd9af74d69ca3479508b5c0707d45f491c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769991"
---
# <a name="certmgr"></a>CertMgr

Gli strumenti di CertMgr sostituiscono DumpCert. Include nuove funzionalità per la gestione [*di*](../secgloss/c-gly.md) [*certificati,*](../secgloss/c-gly.md) elenchi di certificati attendibili (CCL) ed elenchi di [*revoche*](../secgloss/c-gly.md) di certificati (CRL). Lo strumento viene installato nella cartella Bin del percorso di \\ installazione di Microsoft Windows Software Development Kit (SDK).

CertMgr è disponibile come parte di Windows SDK, che è possibile scaricare da <https://go.microsoft.com/fwlink/p/?linkid=84091> .

CertMgr esegue una delle quattro funzioni seguenti, a seconda dell'azione indicata nel comando.

**CertMgr** \[ **-add** \| **-del** \| **-put** \] \[  \] Opzioni \[ **-s** \[ **-r** *RegistryLocation* \] \] *SourceName* \[ **-s** \[ **-r** *RegistryLocation* \] \] \[ *DestinationName*\]

La tabella seguente indica le azioni di base dello strumento CertMgr.



| Flag di azione | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno        | Visualizza certificati, CRL o CCL. Senza flag di azione (solo per la visualizzazione), *SourceName* è il nome dell'archivio certificati o del file contenente gli elementi da visualizzare. L'archivio può essere [*un archivio serializzato*](../secgloss/s-gly.md) (StoreFile) o un archivio di sistema. Per impostazione predefinita, CertMgr visualizza tutti i certificati, gli CRL o i CRL nell'archivio certificati o nel file. *DestinationName non* viene usato per la visualizzazione.<br/>                                                                                                                                                                                                                                                                                                                                  |
| -aggiungere        | Copia certificati, CRL e CRL in un archivio certificati. Quando si **usa -add**, *SourceName è* l'archivio certificati di origine che contiene i certificati, gli CCL e i CRL esistenti. *DestinationName* è l'archivio certificati di destinazione a cui verranno aggiunti i certificati, gli CRL e i CRL. L'archivio di destinazione verrà salvato come archivio [*serializzato,*](../secgloss/s-gly.md) a meno che non venga usata l'opzione **-7,** che salva l'archivio come file [*PKCS*](../secgloss/p-gly.md) \# 7. Si noti che **l'opzione -7** non può essere usata quando l'archivio di destinazione è un archivio di sistema.<br/>                                                                                                                          |
| -del        | Elimina certificati, CRL e CRL da un archivio certificati. Quando si **usa -del**, *SourceName è* l'archivio certificati di origine che contiene i certificati, gli CCL e i CRL esistenti. *DestinationName* è l'archivio certificati di destinazione che conterrà copie dei certificati, degli CRL e dei CRL rimanenti dopo l'eliminazione degli elementi specificati. Se *destinationName* non viene specificato, *SourceName* fungerà anche da archivio di destinazione (verrà modificato). L'archivio di destinazione verrà salvato come archivio [*serializzato,*](../secgloss/s-gly.md) a meno che non venga usata l'opzione **-7,** che salva l'archivio come file PKCS \# 7. Si noti che **l'opzione -7** non può essere usata quando l'archivio di destinazione è un archivio di sistema.<br/> |
| -put        | Salva un [*certificato con codifica X.509,*](../secgloss/x-gly.md) un CTL o un CRL in un file. Quando si **usa -put**, *SourceName è* l'archivio certificati di origine che contiene i certificati, gli CRL e gli CRL esistenti. *DestinationName* è il nome di un file in cui verranno salvati un certificato con codifica [*X.509,*](../secgloss/x-gly.md) CTL e CRL. Se si **usa l'opzione -7,** il file verrà salvato come file PKCS \# 7.<br/>                                                                                                                                                                                                                                                                                             |



 

## <a name="options"></a>Opzioni

Le opzioni seguenti si applicano a tutte le funzioni di CertMgr tranne dove specificato.



| Opzione                     | Flag di azione                                 | Descrizione                                                                                                                                                                                                                                        |
|----------------------------|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-v**                     | none (solo visualizzazione)                         | Modalità dettagliata. Visualizza informazioni dettagliate su certificati, CRL e CRL. L'impostazione predefinita è la visualizzazione di brevi informazioni.                                                                                                                       |
| **-c**                     | all                                         | Usare solo i certificati.                                                                                                                                                                                                                             |
| **-CTL**                   | all                                         | Usare solo gli CCL.                                                                                                                                                                                                                                     |
| **-CRL**                   | all                                         | Usare solo CRL.                                                                                                                                                                                                                                     |
| **-all**                   | **-add-del**<br/> **-put**<br/> | Aggiunge tutte le voci del tipo scelto.                                                                                                                                                                                                               |
| **-e** *encodingType*      | all                                         | Tipo [*di codifica del certificato*](../secgloss/e-gly.md).                                                                                                                                             |
| **-y** *storeProviderType* | all                                         | Tipo di provider dell'archivio.                                                                                                                                                                                                                               |
| **-7**                     | **-add-del**<br/> **-put**<br/> | Salva l'archivio di destinazione come file PKCS \# 7.                                                                                                                                                                                                    |
| **-f** *dwFlags*           | all                                         | Archiviare il flag aperto. Si tratta del *parametro dwFlags* passato a [**CertOpenStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) Il valore predefinito è CERT \_ SYSTEM \_ STORE CURRENT \_ \_ USER. Significativo solo se **è impostato -y.** Per altre informazioni, vedere **CertOpenStore.**         |
| **-n** *commonNameString*  | **-add-del**<br/> **-put**<br/> | Nome comune del certificato. Può essere usato solo con i certificati.                                                                                                                                                                                |
| **-sha1** *sha1Hash*       | **-add-del**<br/> **-put**<br/> | Hash SHA1 del certificato, CTL o CRL da copiare, eliminare o salvare.                                                                                                                                                                         |
| **-s**                     | all                                         | Indica che l'archivio è un archivio di sistema.                                                                                                                                                                                                        |
| **-r** *registryLocation*  | all                                         | Percorso del Registro di sistema dell'archivio certificati di sistema. Significativo solo quando **è impostato -s.** Deve essere impostato su *currentUser (chiave* del Registro di sistema HKEY \_ CURRENT \_ USER) o *localMachine* (chiave del Registro di sistema HKEY \_ LOCAL \_ MACHINE). *currentUser* è l'impostazione predefinita. |
| **-?**                     | all                                         | Visualizza tutte le opzioni.                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

CertMgr è supportato solo in Internet Explorer 4.0 o versione successiva.

CertMgr può copiare, eliminare o salvare uno o più certificati, CRL o CRL. Se è presente più di un elemento in una di queste categorie, l'utente ha tre opzioni:

-   Usare **l'opzione -all** per copiare, eliminare o salvare tutti gli elementi nella categoria indicata.
-   Usare le **opzioni -n** **e -sha1** per identificare in modo univoco l'elemento da copiare, eliminare o salvare.
-   Se **-all** o **-n** e **-sha1** non sono indicati, CertMgr richiede all'utente un elenco di elementi da copiare, eliminare o salvare. L'utente risponde immettendo l'indice dell'elemento da copiare, eliminare o salvare.

Le azioni di CertMgr usano lievi variazioni della sintassi e delle opzioni. È necessario usare la sintassi e le opzioni specifiche di un'azione.

CertMgr funziona con due tipi di archivi certificati: StoreFile e Archivio di sistema. StoreFile può essere uno dei tipi di file seguenti:

-   Un file CTL/CRL/certificato codificato (potrebbe essere codificato in base 64)
-   File PKCS \# 7
-   Documento firmato
-   StoreFile serializzato

Non è necessario specificare il tipo di StoreFile. CertMgr può determinare il tipo StoreFile ed eseguire le azioni appropriate.

Un archivio di sistema è un archivio certificati che si trova normalmente nel Registro di sistema in **currentUser**. L'utente può fare riferimento a un archivio di sistema specificando solo il nome. Non è necessario specificare il tipo di provider dell'archivio certificati. A seconda del tipo di StoreFile o dell'archivio di sistema, CertMgr sceglie il tipo di provider dell'archivio corrispondente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di CertMgr](using-certmgr.md)
</dt> </dl>

 

 
