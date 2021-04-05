---
title: Installazione del gestore di file e flussi
description: Installazione del gestore di file e flussi
ms.assetid: 8d007ea4-b75a-4b3f-965f-8091fcd4cb2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be94137df69ed35b57b1b8fbeb5c9640dd7636d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713597"
---
# <a name="file-and-stream-handler-installation"></a>Installazione del gestore di file e flussi

La libreria AVIFile usa i gestori di flussi e file installati per la lettura e la scrittura di file e flussi AVI. Un gestore viene installato quando risiede nella directory di sistema di Windows e il registro di sistema contiene le informazioni seguenti necessarie per descrivere e identificare un gestore:

-   Identificatore di classe a 16 byte per il gestore
-   Breve descrizione del gestore
-   Nome del file che contiene il gestore
-   Estensione di file che un gestore di file può elaborare
-   Accesso ai file e altre proprietà associate a un gestore di file
-   Codici di quattro caratteri che identificano i tipi di flusso che possono essere elaborati da un gestore di flusso

La libreria AVIFile esegue una query nel registro di sistema per i gestori esterni a un'applicazione durante l'apertura di file e l'accesso ai flussi. Il risultato di una query eseguita correttamente restituisce il nome file di un gestore in grado di elaborare il tipo di file o di flusso specificato nella query. Il registro di sistema elenca ogni gestore creando tre voci il cui formato è il seguente:


```C++
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000-000000000046}] 
@="Wave File reader/writer" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\InprocServer32] 
@="wavefile.dll" 
"ThreadingModel"="Apartment" 
[HKEY_CLASSES_ROOT\Clsid\{00010023-0000-0000-C000- 
000000000046}\AVIFile] 
@="3" 
 
```



Queste voci sono costituite dalle parti seguenti.



| Parte                                   | Descrizione                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY\_CLASSI\_RADICE                    | Identifica la voce radice del registro di sistema.                                                                                                                                               |
| CLSID                                  | Identifica questa voce come identificatore di classe.                                                                                                                                             |
| {00010023-0000-0000-C000-000000000046} | Specifica un identificatore di interfaccia (IID) o un identificatore di classe. Questo valore è un identificatore univoco a 16 byte. L'identificatore può anche essere definito GUID o UUID in altri manuali. |
| Lettura/scrittura file Wave                | Specifica una stringa per descrivere il gestore. Questa stringa può essere visualizzata nelle finestre di dialogo per la selezione di gestori di file e flussi.                                                         |
| InProcServer32                         | Specifica il file (in questo esempio WAVEFILE.DLL) che può essere caricato per gestire questa classe.                                                                                              |
| AVIFile                                | Specifica le proprietà di un gestore di file. In questo esempio, il gestore può leggere e scrivere in un file AVI.                                                                              |



 

Un gestore di file può avere una o più proprietà archiviate nel registro di sistema. Le costanti seguenti identificano le proprietà attualmente associate a un file.



| Costante                        | Descrizione                                                          |
|---------------------------------|----------------------------------------------------------------------|
| \_CANACCEPTNONRGB AVIFILEHANDLER | Indica che un gestore di file può elaborare dati di immagini diversi da RGB. |
| AVIFILEHANDLER \_ CANREAD         | Indica che un gestore di file può aprire un file con accesso in lettura.      |
| \_CANWRITE AVIFILEHANDLER        | Indica che un gestore di file può aprire un file con accesso in scrittura.     |



 

Quando si crea un gestore di file o flussi, è possibile ottenere un nuovo identificatore eseguendo UUIDGEN.EXE. Usare sempre UUIDGEN.EXE per creare un nuovo identificatore. Il numero esadecimale a 16 byte creato da questo eseguibile identificherà in modo univoco il gestore.

La libreria AVIFile usa voci aggiuntive nel registro di sistema per identificare un identificatore di classe basato sull'estensione di file che un gestore di file può elaborare o su un codice di quattro caratteri che un gestore di file o flussi può elaborare. Ad esempio, le voci seguenti associano un identificatore di classe all'estensione di file. WAV e il codice a quattro caratteri "WAVE":


```C++
[HKEY_CLASSES_ROOT\AVIFile\Extensions\WAV] 
@="{00010023-0000-0000-C000-000000000046}" 
[HKEY_CLASSES_ROOT\AVIFile\RIFFHandlers\WAVE] 
@="{00010023-0000-0000-C000-000000000046}" 
 
```



Queste voci sono costituite dalle parti seguenti.



| Parte                                   | Descrizione                                                                                       |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| HKEY\_CLASSI\_RADICE                    | Identifica la voce radice del registro di sistema.                                                        |
| AVIFile                                | Identifica questa voce come una voce utilizzata da AVIFile.                                                |
| Estensioni                             | Specifica l'estensione di file (in questo esempio,. WAV) che un gestore di file può elaborare.             |
| RIFFHandlers                           | Specifica il codice di quattro caratteri, in questo esempio "WAVE", che può essere elaborato da un gestore di file o flussi. |
| {00010023-0000-0000-C000-000000000046} | Specifica un identificatore di interfaccia (IID) o un identificatore di classe.                                      |



 

Se si distribuisce il gestore di flussi o file senza un'applicazione di installazione per installarlo nel sistema dell'utente, è necessario includere un. REG file in modo che l'utente possa installare il gestore. L'utente userà l'editor del registro di sistema per creare le voci del registro di sistema per il gestore di file o di flusso.

Nell'esempio seguente viene illustrato il contenuto di un oggetto tipico. File REG. La prima voce nell'esempio seguente è la stringa descrittiva per il gestore. La seconda voce identifica il file contenente il gestore. La terza voce identifica le proprietà del gestore di file, in questo caso l'accesso in sola lettura ai file. La quarta voce associa il tipo di file elaborato dal gestore, in questo caso i file con un. Estensione del nome file JPG) con l'identificatore di classe.


```C++
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}] 
@="JFIF (JPEG) Files" 
[HKEY_CLASSES_ROOT\Clsid\{5C2B8200-E2C8-1068-B1CA-6066188C6002}]\InprocServer32] 
@="jfiffile.dll" 
[HKEY_CLASSES_ROOT\AVIFile\Extensions\JPG] 
@="{5C2B8200-E2C8-1068-B1CA-6066188C6002}" 
 
```



Quando si crea questo file, salvarlo con un. REG Extension per identificarlo come file di aggiornamento per il registro di sistema. Sostituire anche un IID univoco per il codice a 16 byte usato nell'esempio.

 

 




