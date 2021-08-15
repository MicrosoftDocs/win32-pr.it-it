---
description: Usare la procedura seguente nelle applicazioni legacy per salvare i modelli di file con estensione x e i dati in un file con estensione x.
ms.assetid: 5401b381-3599-465a-b41b-e63b7372fc0e
title: Salvataggio in un file X (legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03070b25c8839ddd17ab698a4f017822004d027d978b5c4ce589491f2e8fb8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797783"
---
# <a name="saving-to-an-x-file-legacy-direct3d-9"></a>Salvataggio in un file X (legacy) (Direct3D 9)

Usare la procedura seguente nelle applicazioni legacy per salvare i modelli di file con estensione x e i dati in un file con estensione x.

1.  Usare la [**funzione DirectXFileCreate**](directxfilecreate.md) per creare un [**oggetto IDirectXFile.**](idirectxfile.md)
2.  Usare il [**metodo IDirectXFile::RegisterTemplates**](idirectxfile--registertemplates.md) per informare il file system DirectX su tutti i modelli che verranno utilizzati.
3.  Usare il [**metodo IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) per creare un [**oggetto IDirectXFileSaveObject.**](idirectxfilesaveobject.md)
4.  Usare il [**metodo IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) per salvare i modelli, se necessario.
5.  Scorrere gli oggetti da salvare. Per ogni oggetto di primo livello, seguire questa procedura.
    -   Usare il [**metodo IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare un [**oggetto IDirectXFileData**](idirectxfiledata.md) come oggetto di primo livello nel file. Se l'oggetto dati di primo livello ha oggetti figlio facoltativi, aggiungerli all'oggetto usando il metodo appropriato del passaggio successivo.
    -   Ogni [**oggetto IDirectXFileData**](idirectxfiledata.md) può avere oggetti figlio facoltativi se il modello lo consente. Gli oggetti figlio possono essere uno qualsiasi dei tre tipi di oggetti: **IDirectXFileData**, [**IDirectXFileDataReference**](idirectxfiledatareference.md)o [**IDirectXFileBinary**](idirectxfilebinary.md). Scorrere in ciclo gli oggetti da salvare, aggiungendo ogni membro figlio facoltativo all'elenco di oggetti nel modo appropriato per il tipo, come illustrato nei passaggi seguenti. Se quindi il tipo di oggetto è Data, chiamare il metodo [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare un oggetto **IDirectXFileData** e quindi chiamare il metodo [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) per aggiungerlo come figlio dell'oggetto. Se il tipo di oggetto è Riferimento dati, chiamare il metodo [**IDirectXFileData::AddDataReference**](idirectxfiledata--adddatareference.md) per creare e aggiungere l'oggetto riferimento ai dati come elemento figlio dell'oggetto. In caso contrario, se il tipo di oggetto è Binary, chiamare il metodo [**IDirectXFileData::AddBinaryObject**](idirectxfiledata--addbinaryobject.md) per creare e aggiungere l'oggetto binario come figlio dell'oggetto.
    -   Chiamare il [**metodo IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) per salvare l'oggetto dati e i relativi elementi figlio.
    -   Rilasciare [**l'oggetto IDirectXFileData.**](idirectxfiledata.md)
6.  Rilasciare [**l'oggetto IDirectXFileSaveObject.**](idirectxfilesaveobject.md)
7.  Rilasciare [**l'oggetto IDirectXFile.**](idirectxfile.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[X File (legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



