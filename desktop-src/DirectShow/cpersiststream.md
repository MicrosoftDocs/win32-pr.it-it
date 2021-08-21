---
description: CPersistStream è la classe di base per le proprietà persistenti dei filtri, ovvero le proprietà dei filtri nei grafici salvati.
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
ms.openlocfilehash: 60a48b35ae1559e9b8dfa718c5bca38689cdf0101ce4a343a907b713c8988de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073581"
---
# <a name="cpersiststream-class"></a>Classe CPersistStream

![Gerarchia di classi cpersiststream](images/pstrm01.png)

`CPersistStream` è la classe di base per le proprietà persistenti dei filtri, ovvero le proprietà dei filtri nei grafici salvati.

Il modo più semplice da usare `CPersistStream` è:

1.  Disporre che il filtro erediti questa classe.
2.  Implementare [**WriteToStream**](cpersiststream-writetostream.md) [**e ReadFromStream**](cpersiststream-readfromstream.md) nella classe . Questi eseguiranno l'override delle funzioni qui, che non fanno altro che fungere da segnaposto.
3.  Modificare **NonDelegatingQueryInterface per** gestire **IPersistStream**.
4.  Implementare [**SizeMax**](cpersiststream-sizemax.md) per restituire un limite superiore al numero di byte di dati che si salvano.

    Se si salvano ™ dati Unicode, tenere presente che WCHAR è di 2 byte.

5.  Quando i dati cambiano, chiamare [**SetDirty**](cpersiststream-setdirty.md).

## <a name="version-numbers"></a>Numeri di versione

A un certo punto è possibile decidere di modificare o estendere il formato dei dati. Sarà quindi necessario avere un numero di versione in tutti i flussi salvati in precedenza, in modo da poter stabilire, quando li si legge, se rappresentano il modulo precedente o nuovo. Per facilitare l'operazione, questa classe scrive e legge un numero di versione. Quando scrive, chiama [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) per informarsi sulla versione del software in uso al momento. In effetti, si tratta di un numero di versione del layout dei dati nel file. Scrive questo come primo elemento nei dati. Se si vuole modificare la versione, implementare (eseguire l'override) **GetSoftwareVersion**. Legge il numero di versione dal file in **mPS \_ dwFileVersion** prima di chiamare [**ReadFromStream,**](cpersiststream-readfromstream.md)quindi in **ReadFromStream** è possibile controllare **mPS \_ dwFileVersion** per verificare se si sta leggendo un file di versione precedente. In genere è consigliabile accettare file la cui versione non è più recente della versione software che li legge.

**CPersistStream implementa** [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Per altre informazioni sull'implementazione, vedere le informazioni di riferimento su COM in Microsoft Platform SDK.



| Membri dati protetti                                          | Descrizione                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| mPS \_ dwFileVersion                                              | Numero di versione del file.                                                   |
| mPS \_ fDirty                                                     | I dati per questo flusso devono essere salvati.                                           |
| Funzioni di membro                                                | Descrizione                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | Costruisce un **oggetto CPersistStream.**                                       |
| [**SetDirty**](cpersiststream-setdirty.md)                     | Indica che l'oggetto deve essere salvato nel flusso.                        |
| Funzioni membro sottoponibili a override                                    | Descrizione                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | Recupera l'identificatore di classe di questo flusso.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Recupera il numero di versione per questo formato di file.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Legge i dati del filtro dal flusso.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Recupera il numero di byte necessari per i dati (senza includere il numero di versione). |
| [**WriteToStream**](cpersiststream-writetostream.md)           | Scrive i dati del filtro nel flusso.                                       |
| Metodi di IPersistStream                                          | Descrizione                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Recupera il numero di byte necessari per i dati (incluso il numero di versione).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Verifica se l'oggetto deve essere salvato.                                           |
| [**Caricamento**](cpersiststream-load.md)                             | Carica i dati dal flusso in memoria.                                   |
| [**Salva**](cpersiststream-save.md)                             | Salva i dati dalla memoria nel flusso.                                     |



 

 

 
