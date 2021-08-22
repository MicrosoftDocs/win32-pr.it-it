---
description: 'Struttura DEVICEDIALOGDATA2: definisce i dati necessari per chiamare un dialogo del dispositivo.'
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Struttura DEVICEDIALOGDATA2 (Wiadefd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA2
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 800f7ceb102cafcad8ddda5204990706b908a4a0137a16143af76a90345b472e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451191"
---
# <a name="devicedialogdata2-structure"></a>Struttura DEVICEDIALOGDATA2

Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD     cbSize;
  IWiaItem2 *pIWiaItemRoot;
  DWORD     dwFlags;
  HWND      hwndParent;
  BSTR      bstrFolderName;
  BSTR      bstrFilename;
  LONG      lNumFiles;
  BSTR      *pbstrFilePaths;
  IWiaItem2 *ppWiaItem;
} DEVICEDIALOGDATA2;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Specifica le dimensioni della struttura in byte.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Punta a [**un'interfaccia IWiaItem2**](-wia-iwiaitem2.md) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Specifica un set di flag che controllano l'operazione della finestra di dialogo. Può essere impostato su uno dei valori seguenti:



| Contrassegno                                 | Significato                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento predefinito.                                                                                                                                                                           |
| IMMAGINE SINGOLA \_ DELLA FINESTRA DI DIALOGO DEL \_ \_ DISPOSITIVO \_ WIA   | Limitare la selezione dell'immagine a una singola immagine nella finestra di dialogo di acquisizione dell'immagine del dispositivo.                                                                                                      |
| FINESTRA DI DIALOGO DEL DISPOSITIVO WIA \_ \_ USA \_ \_ L'INTERFACCIA \_ UTENTE COMUNE | Usare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore. Se l'interfaccia utente del sistema non è disponibile, viene usata l'interfaccia utente del fornitore. Se nessuna delle due interfaccia utente è disponibile, la funzione restituisce E \_ NOTIMPL. |



 

</dd> <dt>

**hwndParent**
</dt> <dd>

Tipo: **HWND**

</dd> <dd>

Specifica l'handle per la finestra padre della finestra di dialogo.

</dd> <dt>

**bstrFolderName**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Specifica il nome della cartella in cui vengono trasferiti i file.

</dd> <dt>

**Bstrfilename**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Specifica il modello di nome file da utilizzare per i file trasferiti da elementi WIA alla cartella di destinazione designata da **bstrFolderName**. È possibile creare un numero arbitrario di nomi di file univoci aggiungendo caratteri aggiuntivi al modello di nome file.

</dd> <dt>

**lNumFiles**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Riceve il numero di stringhe scritte nella matrice **pbstrFilePaths.**

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

Tipo: **BSTR \***

</dd> <dd>

Puntatore a una matrice di puntatori BSTR. Ogni elemento della matrice punta a un BSTR che contiene il nome di destinazione di un file trasferito correttamente nella cartella identificata da bstrFolderName. Il metodo deve allocare l'archiviazione per questo membro.

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

</dd> <dd>

Puntatore [**all'interfaccia IWiaItem2**](-wia-iwiaitem2.md) dell'elemento WIA che trasferisce dati al file o ai file denominati nella matrice **pbstrFilePaths.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




