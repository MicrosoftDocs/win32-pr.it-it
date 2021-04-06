---
description: In questo argomento viene descritto in che modo l'applicazione può specificare l'URL che lo strumento di cattura dei Tablet PC deve ottenere durante l'acquisizione dell'applicazione.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Supporto dello strumento di cattura in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046dd6c8a97d1dacc20065dc1f741610fec13865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883738"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Supporto dello strumento di cattura in Windows Vista

In questo argomento viene descritto in che modo l'applicazione può specificare l'URL che lo strumento di cattura dei Tablet PC deve ottenere durante l'acquisizione dell'applicazione.

## <a name="specifying-the-url-via-registry-key"></a>Specifica dell'URL tramite la chiave del registro di sistema

Lo strumento di cattura consente agli utenti di acquisire un oggetto snip (screenshot) di qualsiasi oggetto sullo schermo e quindi annotare, salvare o condividere l'immagine. Quando i dati vengono salvati in formato HTML o quando vengono inviati a un client di posta elettronica che supporta HTML inline, lo strumento di cattura può aggiungere un URL all'elemento snip se l'applicazione fornisce informazioni su come ottenere l'URL.

Lo strumento di cattura Ottiene l'URL tramite oggetti di accessibilità. Le applicazioni devono specificare le informazioni necessarie nelle seguenti chiavi del registro di sistema:

HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ lo strumento \\ di cattura LinkFingerprints,

E devono creare una sottochiave il cui nome corrisponda alla classe della finestra da cui deve essere ottenuto il collegamento. Il nome della classe della finestra deve essere la finestra in primo piano dell'applicazione.

HKLM \\ software \\ Microsoft \\ Windows \\ TabletPC \\ lo strumento di cattura \\ LinkFingerprints\\<Window Class Name>

### <a name="window-class-key-details"></a>Dettagli chiave classe finestra

Sotto la chiave della classe della finestra, è necessario impostare i valori appropriati per indicare che lo strumento di cattura deve rilevare l'oggetto di accessibilità corretto.



| VALUE                        | TYPE                  | MASCHERA            | INFORMAZIONI ARCHIVIATE                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | REG \_ DWORD<br/> |                 | Indica i campi seguenti da controllare<br/> |
| Nome<br/>              | REG \_ SZ<br/>    | 0x02<br/> | Nome accessibilità<br/>                               |
| Descrizione<br/>       | REG \_ SZ<br/>    | 0x04<br/> | Descrizione accessibilità<br/>                        |
| Ruolo<br/>              | REG \_ DWORD<br/> | 0x08<br/> | Ruolo di accessibilità<br/>                               |
| ParentName<br/>        | REG \_ SZ<br/>    | 0x10<br/> | Nome di accessibilità dell'elemento padre<br/>                     |
| ParentValue<br/>       | REG \_ SZ<br/>    | 0x20<br/> | Valore di accessibilità dell'elemento padre<br/>                    |
| ParentRole<br/>        | REG \_ DWORD<br/> | 0x40<br/> | Ruolo di accessibilità dell'elemento padre<br/>                     |
| ParentDescription<br/> | REG \_ SZ<br/>    | 0x80<br/> | Descrizione dell'accessibilità dell'elemento padre<br/>              |



 

Inoltre, se è impostato il valore di bit della maschera 0x1, l'URL deve essere prelevato dal nome dell'accessibilità; in caso contrario, l'URL deve essere tratto dal valore di accessibilità.

Se l'applicazione usa stringhe localizzate per i \_ valori reg SZ precedenti, la stringa deve essere specificata come stringa indiretta usando il formato seguente:

@filename, risorsa

La stringa viene estratta dal file denominato, usando il valore della risorsa come localizzatore. Se il valore della risorsa è zero o maggiore, il numero diventa l'indice della stringa nel file binario. Se il numero è negativo, diventa un identificatore di risorsa (ID).

> [!Note]  
> Le costanti Role sono reperibili in oleacc. h nella Windows SDK. I valori del registro di sistema descritti sono specifici di Windows Vista.

 

 

 




