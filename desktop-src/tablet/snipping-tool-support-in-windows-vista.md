---
description: Questo argomento descrive in che modo l'applicazione può specificare l'URL che l'Strumento di cattura Tablet PC deve ottenere durante l'acquisizione dell'applicazione.
ms.assetid: e31e63e8-8f6b-41f7-8bd6-afc5ca32456b
title: Strumento di cattura in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb2c24901524500df97461f3b3acf88d9a51f73cc24134955c1df866a457a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966770"
---
# <a name="snipping-tool-support-in-windows-vista"></a>Strumento di cattura in Windows Vista

Questo argomento descrive in che modo l'applicazione può specificare l'URL che l'Strumento di cattura Tablet PC deve ottenere durante l'acquisizione dell'applicazione.

## <a name="specifying-the-url-via-registry-key"></a>Specifica dell'URL tramite la chiave del Registro di sistema

Strumento di cattura consente agli utenti di acquisire una cattura di schermata di qualsiasi oggetto sullo schermo e quindi annotare, salvare o condividere l'immagine. Quando i dati vengono salvati in formato HTML o quando vengono inviati a un client di posta elettronica che supporta HTML inline, Strumento di cattura può aggiungere un URL al frammento se l'applicazione fornisce informazioni su come ottenere l'URL.

Strumento di cattura ottiene l'URL tramite oggetti di accessibilità. Le applicazioni devono specificare le informazioni necessarie nelle chiavi del Registro di sistema seguenti:

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Strumento di cattura \\ \\ LinkFingerprints,

E deve creare una sottochiave il cui nome è uguale alla classe della finestra da cui deve essere ottenuto il collegamento. Il nome della classe della finestra deve essere la finestra più in alto dell'applicazione.

HKLM \\ Software Microsoft Windows \\ \\ \\ TabletPC Strumento di cattura \\ \\ LinkFingerprints\\<Window Class Name>

### <a name="window-class-key-details"></a>Dettagli chiave classe finestra

Sotto la chiave della classe della finestra, è necessario impostare i valori appropriati per indicare Strumento di cattura deve rilevare l'oggetto di accessibilità corretto.



| VALORE                        | TYPE                  | Maschera            | INFORMAZIONI ARCHIVIATE                                          |
|------------------------------|-----------------------|-----------------|-------------------------------------------------------------|
| Mask<br/>              | REG \_ DWORD<br/> |                 | Indica quale dei campi seguenti controllare<br/> |
| Nome<br/>              | REG \_ SZ<br/>    | 0x02<br/> | Nome accessibilità<br/>                               |
| Descrizione<br/>       | REG \_ SZ<br/>    | 0x04<br/> | Descrizione dell'accessibilità<br/>                        |
| Ruolo<br/>              | REG \_ DWORD<br/> | 0x08<br/> | Ruolo accessibilità<br/>                               |
| ParentName<br/>        | REG \_ SZ<br/>    | 0x10<br/> | Nome di accessibilità dell'elemento padre<br/>                     |
| Valore padre<br/>       | REG \_ SZ<br/>    | 0x20<br/> | Valore di accessibilità dell'elemento padre<br/>                    |
| Ruolo padre<br/>        | REG \_ DWORD<br/> | 0x40<br/> | Ruolo di accessibilità dell'elemento padre<br/>                     |
| Descrizione padre<br/> | REG \_ SZ<br/>    | 0x80<br/> | Descrizione dell'accessibilità dell'elemento padre<br/>              |



 

Inoltre, se il valore di bit della maschera 0x1 è impostato, l'URL deve essere derivato dal nome di accessibilità; In caso contrario, l'URL deve essere tratto dal valore di accessibilità.

Se l'applicazione usa stringhe localizzate per i valori REG SZ precedenti, la stringa deve essere fornita come stringa indiretta \_ usando il formato seguente:

@filenameRisorsa

La stringa viene estratta dal file denominato , usando il valore della risorsa come localizzatore. Se il valore della risorsa è zero o maggiore, il numero diventa l'indice della stringa nel file binario. Se il numero è negativo, diventa un identificatore di risorsa (ID).

> [!Note]  
> Le costanti di ruolo sono disponibili in oleacc.h in Windows SDK. I valori del Registro di sistema descritti sono specifici Windows Vista.

 

 

 




