---
title: IPropertySetStorage-implementazione del file system NTFS
description: NTFS versione 5,0 fornisce un'implementazione di IPropertySetStorage per i file in un volume NTFS quando i file non sono file composti.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd STG, implementazioni, NTFS file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0d647b9cb804376a9efeb687b1524585ee938d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299911"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage-implementazione del file system NTFS

NTFS versione 5,0 fornisce un'implementazione di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per i file in un volume NTFS quando i file non sono file composti. L'implementazione NTFS è equivalente all' [implementazione del file composto](ipropertysetstorage-compound-file-implementation.md). Per ulteriori informazioni sulle eccezioni, vedere la sezione Osservazioni.

**Per ottenere un puntatore all'implementazione NTFS di IPropertySetStorage**

1.  Chiamare [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) e specificare **il \_ file STGFMT** nel parametro *grfFlags* per creare un nuovo file.
2.  Chiamare [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) e specificare il **\_ file STGFMT** o **STGFMT \_ qualsiasi** valore di enumerazione nel parametro *grfFlags* per aprire un file esistente.

Tuttavia, non è possibile ottenere l'implementazione NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per un file composto. Quando si apre un file composto con [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), se si specifica il valore di enumerazione **\_ file STGFMT** si verifica un errore.

Inoltre, i set di proprietà semplici non possono essere sottoposti a transazione. Ovvero, non è possibile specificare **STGM \_ transazionale** nel parametro *grfMode* dei metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , a meno che non si specifichi anche **PROPSETFLAG \_ nonsimple** nel parametro *grfFlags* . L'oggetto di archiviazione del set di proprietà non supporta l'elaborazione delle transazioni.

## <a name="when-to-use"></a>Utilizzo

Chiamare i metodi [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare, aprire o eliminare set di proprietà nella risorsa di archiviazione del set di proprietà NTFS corrente. Esiste anche un metodo, [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), che fornisce un puntatore a un enumeratore che può essere usato per enumerare i set di proprietà nell'archivio.

## <a name="compatibility"></a>Compatibilità

Le implementazioni NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sono disponibili a partire da Windows 2000. Le versioni precedenti non possono accedere a questi set di proprietà.

L'implementazione NTFS archivia i set di proprietà in flussi alternativi di un file NTFS. Quando viene copiato il file principale, è necessario copiare i flussi alternativi.

> [!Caution]  
> Non tutti i file System supportano tali flussi. Se un file NTFS con set di proprietà viene copiato in un volume FAT, vengono copiati solo i dati nel file; il set di proprietà viene perso. In questo caso, la funzione [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) non restituisce un errore.

 

> [!Caution]  
> Se il computer che esegue la copia del file non è un computer in cui è in esecuzione Windows 2000 o versione successiva, è possibile che i set di proprietà vadano persi. Se, ad esempio, un computer che esegue il sistema operativo Windows 95 copia un file NTFS, il set di proprietà viene perso anche se anche il file di destinazione si trova in un volume NTFS.

 

## <a name="methods"></a>Metodi

L'implementazione del file system NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supporta i metodi seguenti.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crea un nuovo set di proprietà nell'archivio file NTFS corrente e, in restituzione, fornisce un puntatore di interfaccia all'implementazione del file NTFS [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . La modalità di condivisione specificata nel parametro *grfMode* deve essere **STGM \_ share \_ Exclusive**.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Apre un set di proprietà esistente nell'archivio della proprietà corrente. Al ritorno, fornisce un puntatore di interfaccia all'implementazione del file NTFS di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). La modalità di condivisione specificata nel parametro *grfMode* deve essere **STGM \_ share \_ Exclusive**.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D Elimina**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Elimina un set di proprietà nell'archivio della proprietà corrente.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crea un oggetto utilizzato per enumerare le strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Ogni struttura **STATPROPSETSTG** fornisce dati su un singolo set di proprietà.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le implementazioni NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) archiviano i set di proprietà in un file senza influire sul contenuto di tale file. Se, ad esempio, si crea un set di proprietà in un file HTML denominato Default.htm, il file viene comunque visualizzato correttamente in una Web browser. Ovvero, le modifiche apportate a un file utilizzando queste due interfacce non sono rilevabili quando si accede a un file con la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

L'implementazione NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) fornisce un'implementazione sicura quando viene usata per scrivere set di proprietà in un file in un volume ntfs versione 5,0. Tali set di proprietà non possono essere danneggiati dall'implementazione anche in caso di errore di sistema. Se, ad esempio, l'alimentazione a un sistema ha esito negativo durante una chiamata a [**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) mentre il set di proprietà viene scaricato sul disco, il set di proprietà non viene mai lasciato in uno stato intermedio. La versione precedente del set di proprietà rimane o tutti gli aggiornamenti vengono salvati.

L'implementazione NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) differisce dall'implementazione del file composto nei modi seguenti:

-   Una struttura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) ottenuta dall'interfaccia [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) contiene un membro **CLSID** il cui valore è sempre zero (**CLSID \_ null**). Con l'implementazione del file composto, viene restituito il membro **CLSID** corretto per i set di proprietà non semplici (vedere [oggetti di archiviazione e di flusso per un set di proprietà](storage-vs--stream-for-a-property-set.md)).
-   Quando si ottiene un'implementazione NTFS del puntatore a interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) utilizzando la funzione [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , il parametro *grfMode* deve rispettare le stesse regole dell'implementazione del file composto.

    Inoltre, è possibile che non vengano utilizzati i flag seguenti:

    **STGM \_ SIMPLE**, **STGM \_ transazionale**, **STGM \_ Convert**, **STGM \_ Priority** e **STGM \_ DELETEONRELEASE**.

-   Quando un'interfaccia [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS viene ottenuta dalle funzioni [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , le modalità di condivisione si applicano principalmente ad altre istanze di tale interfaccia e non alle istanze di che aprono il file stesso. Se, ad esempio, un'interfaccia **IPROPERTYSETSTORAGE** NTFS viene aperta chiamando la funzione **StgOpenStorageEx** , con il parametro *grfMode* impostato su **STGM \_ ReadWrite \| STGM \_ share \_ Exclusive**, è possibile aprire il file con la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

    Tali istanze simultanee di apertura di questa interfaccia sono soggette ai vincoli seguenti: il parametro *dwShareMode* nella funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) deve specificare il flag di **\_ \_ lettura della condivisione file** e il parametro *dwAccess* non deve specificare il flag **Delete** . Inoltre, le funzioni [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) non devono essere chiamate su un file per il quale queste interfacce del set di proprietà sono aperte, perché queste funzioni richiedono l'accesso **Delete** al file.

-   Se un metodo [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS viene aperto in sola lettura e il file attualmente non include set di proprietà, l'oggetto restituito non conterrà effettivamente il file aperto. Di conseguenza, altre aperture del file avranno esito positivo, anche se la modalità di condivisione dell'operazione di apertura originale lo rifiuterà.

    Esempio Se un [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS viene aperto in modalità **STGM \_ Read \| STGM \_ share \_ Exclusive** e il file non dispone di alcun set di proprietà, sarà possibile aprire contemporaneamente il file **STGM ReadWrite STGM \_ \| \_ share \_ Exclusive**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IPropertyStorage-implementazione del file system NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Costanti PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 