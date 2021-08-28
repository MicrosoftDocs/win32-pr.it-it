---
title: Implementazione del file system IPropertySetStorage-NTFS
description: NTFS versione 5.0 fornisce un'implementazione di IPropertySetStorage per i file in un volume NTFS quando i file stessi non sono file composti.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd Stg , implementazioni, ntfs file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0794e2905cd9e8bd06804decb756b3f1f639c75e837b2d5f3181bb73939717f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683041"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>Implementazione del file system IPropertySetStorage-NTFS

NTFS versione 5.0 fornisce un'implementazione di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per i file in un volume NTFS quando i file stessi non sono file composti. L'implementazione NTFS equivale [all'implementazione di file compositi](ipropertysetstorage-compound-file-implementation.md). Per altre informazioni sulle eccezioni, vedere Osservazioni.

**Per ottenere un puntatore all'implementazione NTFS di IPropertySetStorage**

1.  Chiamare [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) e specificare **STGFMT \_ FILE** nel *parametro grfFlags* per creare un nuovo file.
2.  Chiamare [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) e specificare il valore di enumerazione **STGFMT \_ FILE** o **STGFMT \_ ANY** nel parametro *grfFlags* per aprire un file esistente.

Tuttavia, non è possibile ottenere l'implementazione NTFS [**di IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per un file composto. Quando si apre un file composto [**con StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), se si specifica il valore di **enumerazione STGFMT \_ FILE** viene generato un errore.

Inoltre, i set di proprietà semplici non possono essere transazionati. In altre parole, non è possibile specificare **STGM \_ TRANSACTED** nel parametro *grfmode* dei metodi [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) a meno che non si specifica anche **PROPSETFLAG \_ NONSIMPLE** nel *parametro grfFlags.* L'oggetto di archiviazione del set di proprietà stesso non supporta l'elaborazione delle transazioni.

## <a name="when-to-use"></a>Utilizzo

Chiamare i [**metodi IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare, aprire o eliminare set di proprietà nell'archiviazione corrente del set di proprietà NTFS. Esiste anche un metodo, [**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), che fornisce un puntatore a un enumeratore che può essere usato per enumerare i set di proprietà nell'archiviazione.

## <a name="compatibility"></a>Compatibilità

Le implementazioni NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sono disponibili a partire Windows 2000. Le versioni precedenti non possono accedere a questi set di proprietà.

L'implementazione NTFS archivia i set di proprietà in flussi alternativi di un file NTFS. I flussi alternativi devono essere copiati quando viene copiato il file principale.

> [!Caution]  
> Non tutti i file system supportano tali flussi. Se un file NTFS con set di proprietà viene copiato in un volume FAT, vengono copiati solo i dati nel file. il set di proprietà viene perso. In [**questo caso,**](/windows/desktop/api/winbase/nf-winbase-copyfile) la funzione CopyFile non restituisce un errore.

 

> [!Caution]  
> Se il computer che esegue la copia del file non è un computer Windows 2000 o versione successiva, i set di proprietà potrebbero essere persi. Ad esempio, se un computer in esecuzione nel sistema operativo Windows 95 copia un file NTFS, il set di proprietà viene perso anche se il file di destinazione si trova anche in un volume NTFS.

 

## <a name="methods"></a>Metodi

L'file system NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supporta i metodi seguenti.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crea un nuovo set di proprietà nell'archivio file NTFS corrente e, in caso di restituzione, fornisce un puntatore a interfaccia all'implementazione del file NTFS [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) La modalità di condivisione specificata nel *parametro grfmode* deve essere **STGM \_ SHARE \_ EXCLUSIVE.**

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Apre un set di proprietà esistente nell'archivio delle proprietà corrente. In caso di restituzione, fornisce un puntatore a interfaccia all'implementazione del file NTFS [**di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). La modalità di condivisione specificata nel *parametro grfmode* deve essere **STGM \_ SHARE \_ EXCLUSIVE.**

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Elimina un set di proprietà nell'archivio delle proprietà corrente.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crea un oggetto utilizzato per enumerare [**le strutture STATPROPSETSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Ogni **struttura STATPROPSETSTG** fornisce dati su un singolo set di proprietà.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le implementazioni NTFS dei set di proprietà [**dell'archivio IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) in un file senza influire sul contenuto di tale file. Ad esempio, se si crea un set di proprietà in un file HTML denominato Default.htm, tale file viene comunque visualizzato correttamente in un Web browser. In altre parole, le modifiche apportate a un file usando queste due interfacce non sono rilevabili quando si accede a un file con la [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

L'implementazione NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) fornisce un'implementazione sicura quando viene usata per scrivere set di proprietà in un file in un volume NTFS versione 5.0. Tali set di proprietà non possono essere danneggiati dall'implementazione anche in caso di errore di sistema. Ad esempio, se l'alimentazione a un sistema non riesce durante una chiamata a [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) mentre il set di proprietà viene scaricato sul disco, il set di proprietà non viene mai lasciato in uno stato intermedio. La versione precedente del set di proprietà rimane o tutti gli aggiornamenti vengono salvati.

L'implementazione NTFS [**di IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) differisce dall'implementazione di file compositi nei modi seguenti:

-   Una [**struttura STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) ottenuta dall'interfaccia [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) contiene un membro **clsid** il cui valore è sempre zero (**CLSID \_ NULL**). Con l'implementazione del file composto, viene restituito il membro **clsid** corretto per i set di proprietà non semplici (vedere i set di proprietà Archiviazione e [Stream Objects per un set](storage-vs--stream-for-a-property-set.md)di proprietà).
-   Quando si ottiene un'implementazione NTFS del puntatore a interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) usando la funzione [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) il parametro *grfmode* deve seguire le stesse regole dell'implementazione del file composto.

    Non è inoltre possibile usare i flag seguenti:

    **STGM \_ SIMPLE,** **STGM \_ TRANSACTED,** **STGM \_ CONVERT,** **STGM \_ PRIORITY** e **STGM \_ DELETEONRELEASE.**

-   Quando [**un'interfaccia IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS viene ottenuta dalle funzioni [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) le modalità di condivisione si applicano principalmente ad altre istanze di tale interfaccia e non alle istanze di apertura del file stesso. Ad esempio, se un'interfaccia **IPropertySetStorage** NTFS viene aperta chiamando la funzione **StgOpenStorageEx,** con il parametro *grfmode* impostato su **STGM \_ READWRITE \| STGM \_ SHARE \_ EXCLUSIVE,** è possibile aprire il file con la [**funzione CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

    Tali istanze simultanee di apertura di questa interfaccia sono soggette ai vincoli seguenti: il *parametro dwShareMode* nella funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) deve specificare il flag **FILE SHARE \_ \_ READ** e il *parametro dwAccess* non deve specificare il flag **DELETE.** Inoltre, le [**funzioni DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) e [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) non devono essere chiamate in un file per cui sono aperte queste interfacce del set di proprietà, perché queste funzioni richiedono l'accesso **DELETE** al file.

-   Se un metodo [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS viene aperto in sola lettura e il file non dispone attualmente di set di proprietà, l'oggetto restituito non contenerà effettivamente l'apertura del file. Di conseguenza, le altre aperture del file avranno esito positivo, anche se la modalità di condivisione dell'operazione di apertura originale lo rifiuterebbe in caso contrario.

    Esempio; se un [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS viene aperto in modalità **STGM \_ READ STGM SHARE \| \_ \_ EXCLUSIVE** e il file non dispone di set di proprietà, sarà possibile aprire contemporaneamente il file **STGM \_ READWRITE \| STGM \_ SHARE \_ EXCLUSIVE**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione del file system IPropertyStorage-NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Costanti PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 