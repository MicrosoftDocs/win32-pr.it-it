---
description: CPersistStream è la classe base per le proprietà permanenti dei filtri, ovvero le proprietà di filtro nei grafici salvati.
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Classe CPersistStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520785"
---
# <a name="cpersiststream-class"></a>Classe CPersistStream

![gerarchia di classi cpersiststream](images/pstrm01.png)

`CPersistStream` è la classe base per le proprietà permanenti dei filtri, ovvero le proprietà di filtro nei grafici salvati.

Il modo più semplice per usare `CPersistStream` è:

1.  Disporre che il filtro erediti questa classe.
2.  Implementare [**WriteToStream**](cpersiststream-writetostream.md) e [**ReadFromStream**](cpersiststream-readfromstream.md) nella classe. Queste funzioni eseguiranno l'override delle funzioni, che non eseguono alcuna operazione, ma fungono da segnaposto.
3.  Modificare il **NonDelegatingQueryInterface** per gestire **IPersistStream**.
4.  Implementare [**SizeMax**](cpersiststream-sizemax.md) per restituire un limite superiore per il numero di byte di dati salvati.

    Se si salvano i dati™ Unicode, tenere presente che WCHAR è di 2 byte.

5.  Quando i dati vengono modificati, chiamare [**sedirty**](cpersiststream-setdirty.md).

## <a name="version-numbers"></a>Numeri di versione

A un certo punto è possibile decidere di modificare o estendere il formato dei dati. Si desidera quindi avere un numero di versione in tutti i flussi salvati precedenti, in modo da poter indicare, quando vengono letti, se rappresentano il form precedente o nuovo. Per semplificare questa operazione, questa classe scrive e legge un numero di versione. Quando scrive, viene chiamato [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) per richiedere la versione del software in uso al momento. (In effetti, si tratta di un numero di versione del layout dei dati nel file). Scrive come prima cosa nei dati. Se si desidera modificare la versione, implementare (override) **GetSoftwareVersion**. Il numero di versione viene letto dal file in **MP \_ dwFileVersion** prima di chiamare [**ReadFromStream**](cpersiststream-readfromstream.md), quindi in **ReadFromStream** è possibile controllare **mPS \_ dwFileVersion** per verificare se si sta leggendo un file di versione precedente. In genere è necessario accettare i file la cui versione non è più recente rispetto alla versione del software che li sta leggendo.

**CPersistStream** implementa [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Per ulteriori informazioni sull'implementazione, vedere la Guida di riferimento a COM in Microsoft Platform SDK.



| Membri dati protetti                                          | Descrizione                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| \_DwFileVersion mPS                                              | Numero di versione del file.                                                   |
| \_FDirty mPS                                                     | I dati per questo flusso devono essere salvati.                                           |
| Funzioni di membro                                                | Descrizione                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | Costruisce un oggetto **CPersistStream** .                                       |
| [**SetDirty**](cpersiststream-setdirty.md)                     | Indica che l'oggetto deve essere salvato nel flusso.                        |
| Funzioni membro sottoponibili a override                                    | Descrizione                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | Recupera l'identificatore di classe di questo flusso.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Recupera il numero di versione per questo formato di file.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Legge i dati del filtro dal flusso.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Recupera il numero di byte necessari per i dati, escluso il numero di versione. |
| [**WriteToStream**](cpersiststream-writetostream.md)           | Scrive i dati del filtro nel flusso.                                       |
| Metodi IPersistStream                                          | Descrizione                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Recupera il numero di byte necessari per i dati (incluso il numero di versione).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Controlla se l'oggetto deve essere salvato.                                           |
| [**Caricamento**](cpersiststream-load.md)                             | Carica i dati dal flusso in memoria.                                   |
| [**Salva**](cpersiststream-save.md)                             | Salva i dati dalla memoria al flusso.                                     |



 

 

 
