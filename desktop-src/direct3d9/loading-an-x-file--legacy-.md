---
description: Per caricare un file con estensione x, attenersi alla procedura seguente in applicazioni legacy.
ms.assetid: 2b975873-2e5d-4c64-a022-d2098c3d95b8
title: Caricamento di un file X (legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ed54afdc7d1aa18fdde992a0799a8990a49c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521169"
---
# <a name="loading-an-x-file-legacy-direct3d-9"></a>Caricamento di un file X (legacy) (Direct3D 9)

Per caricare un file con estensione x, attenersi alla procedura seguente in applicazioni legacy.

1.  Usare la funzione [**DirectXFileCreate**](directxfilecreate.md) per creare un oggetto [**IDirectXFile**](idirectxfile.md) .
2.  Se i modelli sono presenti nel file DirectX che verrà caricato, usare il metodo [**IDirectXFile:: RegisterTemplates**](idirectxfile--registertemplates.md) per registrare tali modelli.
3.  Usare il metodo [**IDirectXFile:: CreateEnumObject**](idirectxfile--createenumobject.md) per creare un oggetto enumeratore [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .
4.  Scorrere gli oggetti nel file. Per ogni oggetto, seguire questa procedura.
    1.  Usare il metodo [**IDirectXFileEnumObject:: GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md) per recuperare ciascun oggetto [**IDirectXFileData**](idirectxfiledata.md) .
    2.  Usare il metodo [**IDirectXFileData:: GetType**](idirectxfiledata--gettype.md) per recuperare il tipo di dati.
    3.  Caricare i dati usando il metodo [**IDirectXFileData:: GetData**](idirectxfiledata--getdata.md) .
    4.  Se l'oggetto dispone di membri facoltativi, recuperare i membri facoltativi chiamando il metodo [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) .
    5.  Rilasciare l'oggetto [**IDirectXFileData**](idirectxfiledata.md) .
5.  Rilasciare l'oggetto [**IDirectXFileEnumObject**](idirectxfileenumobject.md) .
6.  Rilasciare l'oggetto [**IDirectXFile**](idirectxfile.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File X (legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



