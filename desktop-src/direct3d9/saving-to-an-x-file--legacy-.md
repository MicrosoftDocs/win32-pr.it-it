---
description: Utilizzare la procedura seguente in applicazioni legacy per salvare i modelli di file e i dati con estensione x in un file con estensione x.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Salvataggio in un file X (legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f824c8e3ab9cd360a93d3f69fd1a2352548ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341696"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Salvataggio in un file X (legacy) (Direct3D 9)

Utilizzare la procedura seguente in applicazioni legacy per salvare i modelli di file e i dati con estensione x in un file con estensione x.

1.  Usare la funzione [**DirectXFileCreate**](directxfilecreate.md) per creare un oggetto [**IDirectXFile**](idirectxfile.md) .
2.  Usare il metodo [**IDirectXFile:: RegisterTemplates**](idirectxfile--registertemplates.md) per informare il file System DirectX su tutti i modelli che saranno usati.
3.  Usare il metodo [**IDirectXFile:: CreateSaveObject**](idirectxfile--createsaveobject.md) per creare un oggetto [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) .
4.  Se lo si desidera, utilizzare il metodo [**IDirectXFileSaveObject:: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) per salvare i modelli.
5.  Scorrere gli oggetti da salvare. Per ogni oggetto di primo livello, seguire questa procedura.
    -   Usare il metodo [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare un oggetto [**IDirectXFileData**](idirectxfiledata.md) come oggetto di primo livello nel file. Se l'oggetto dati di primo livello include oggetti figlio facoltativi, aggiungerli all'oggetto usando il metodo appropriato dal passaggio successivo.
    -   Ogni oggetto [**IDirectXFileData**](idirectxfiledata.md) può disporre di oggetti figlio facoltativi se ne consente il modello. Gli oggetti figlio possono essere uno dei tre tipi di oggetti: **IDirectXFileData**, [**IDirectXFileDataReference**](idirectxfiledatareference.md)o [**IDirectXFileBinary**](idirectxfilebinary.md). Scorrere gli oggetti che è necessario salvare, aggiungendo ogni membro figlio facoltativo all'elenco di oggetti nel modo appropriato al tipo, come illustrato nei passaggi seguenti. Quindi, se il tipo di oggetto è dati, chiamare il metodo [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare un oggetto **IDirectXFileData** e quindi chiamare il metodo [**IDirectXFileData:: AddDataObject**](idirectxfiledata--adddataobject.md) per aggiungerlo come figlio dell'oggetto. Se il tipo di oggetto è riferimento ai dati, chiamare il metodo [**IDirectXFileData:: AddDataReference**](idirectxfiledata--adddatareference.md) per creare e aggiungere l'oggetto riferimento ai dati come figlio dell'oggetto. In alternativa, se il tipo di oggetto è binario, chiamare il metodo [**IDirectXFileData:: AddBinaryObject**](idirectxfiledata--addbinaryobject.md) per creare e aggiungere l'oggetto binario come figlio dell'oggetto.
    -   Chiamare il metodo [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) per salvare l'oggetto dati e i relativi elementi figlio.
    -   Rilasciare l'oggetto [**IDirectXFileData**](idirectxfiledata.md) .
6.  Rilasciare l'oggetto [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) .
7.  Rilasciare l'oggetto [**IDirectXFile**](idirectxfile.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File X (legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



