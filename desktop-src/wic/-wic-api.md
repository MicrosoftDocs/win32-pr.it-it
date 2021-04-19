---
description: Windows Imaging Component (WIC) fornisce un'API basata su Component Object Model (COM) per l'utilizzo in C e C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Panoramica dell'API WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313437"
---
# <a name="wic-api-overview"></a>Panoramica dell'API WIC

Windows Imaging Component (WIC) fornisce un'API basata su Component Object Model (COM) per l'utilizzo in C e C++. L'API WIC espone un'ampia gamma di funzionalità correlate all'immagine, tra cui:

-   Codec predefiniti per i formati di immagine Web standard.
-   Supporto incorporato per i formati di metadati standard.
-   Ampia gamma di supporto per il formato pixel.
-   Supporto per colori elevati; inclusi i formati di intervallo esteso a 30 bit, a 32 bit e di precisione elevata e a 48 bit e i formati pixel a gamma ampia.
-   Framework estensibile per codec di immagini, formati pixel e formati di metadati.

Questo argomento contiene gli argomenti seguenti.

-   [File di intestazione WIC](#wic-header-files)
-   [File di libreria](#library-files)
-   [Class factory](#class-factories)
-   [Componenti per la creazione di immagini](#imaging-components)
-   [Vedere anche](#see-also)

## <a name="wic-header-files"></a>File di intestazione WIC

Le API WIC sono definite nei file di intestazione e IDL (Interface Definition Language) seguenti:



| File              | Descrizione                                          |
|-------------------|------------------------------------------------------|
| wincodec. h        | Definisce le versioni C e C++ delle API WIC primarie.  |
| wincodec. idl      | Definisce le interfacce WIC primarie.                  |
| wincodecsdk. h     | Definisce le versioni C e C++ delle API WIC dei metadati. |
| wincodecsdk. idl   | Definisce le interfacce dei metadati WIC.                 |
| \_proxy wincodec. h | Definisce le esportazioni del proxy WIC.                       |



 

Per usare WIC, le applicazioni devono includere wincodec. h e/o wincodecsdk. h, a seconda dell'API necessaria per l'applicazione.

## <a name="library-files"></a>File di libreria

File della libreria WIC:



| File              | Descrizione                                                            |
|-------------------|------------------------------------------------------------------------|
| windowscodecs. lib | Libreria di importazione fornita da Windows Software Development Kit (SDK). |
| windowscodecs.dll | Libreria di implementazione azionaria fornita dal sistema operativo.         |



 

Per eseguire il collegamento alle API WIC, l'applicazione deve includere windowscodec. lib come dipendenza aggiuntiva del linker.

## <a name="class-factories"></a>Class factory

Nella tabella seguente vengono descritte le due class factory COM fornite dalle API WIC per la creazione di componenti WIC.



| Interfaccia Factory                                               | Descrizione                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | Class factory primario per lo sviluppo di applicazioni mediante componenti WIC. Questa factory crea componenti come decodificatori di immagini, codificatori e flussi.   |
| [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | Class factory di destinazione per gli sviluppatori di componenti WIC. I componenti creati da questa factory vengono usati principalmente per lo sviluppo di codec e gestori di metadati. |



 

Per creare una class factory, utilizzare la funzione com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . Nell'esempio seguente viene illustrata la creazione di WIC Imaging Factory.


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a>Componenti per la creazione di immagini

Le API WIC forniscono diversi tipi di componenti per la creazione di immagini. Nella tabella seguente vengono descritti alcuni dei componenti di WIC comuni. Per un elenco completo dei componenti disponibili, vedere [interfacce WIC](-wic-codec-ifaces.md).



| Tipo di componente                                                      | Descrizione                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**Bitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | Rappresenta una rappresentazione in memoria scrivibile di un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource). |
| [**Decodificatore**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | Usato per decodificare i dati immagine da un flusso in un formato utile per l'elaborazione di immagini.                    |
| [**Encoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | Scrive i dati dell'immagine in un flusso.                                                                                |
| [**Stream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | Utilizzato per leggere e scrivere dati da un file, da una risorsa di rete, da un blocco di memoria e così via.                      |
| [**Convertitore di formato**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | Utilizzato per eseguire la conversione da un formato pixel a un altro.                                                             |
| [**Lettore di query dei metadati**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | Utilizzato per leggere i metadati di un'immagine o di un frame di immagine.                                                             |
| [**Writer di query dei metadati**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | Utilizzato per scrivere i metadati in un'immagine o in un frame di immagine.                                                            |



 

## <a name="see-also"></a>Vedere anche

[Riferimenti](-wic-codec-reference.md)


[Esempi ed esempi di codice](-wic-samples.md)


 

 
