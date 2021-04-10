---
description: Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.
ms.assetid: 544238de-310f-4fc3-b519-bb4e6b309272
title: Struttura DEVICEDIALOGDATA2 (Wiadefd. h)
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
ms.openlocfilehash: f4ab56114054b4f69a21fd9f4c05a1e119bab5da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050039"
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

Specifica la dimensione in byte della struttura.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

Punta a un'interfaccia [_ *IWiaItem2* *](-wia-iwiaitem2.md) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.

</dd> <dt>

**dwFlags**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Specifica un set di flag che controllano l'operazione della finestra di dialogo. Può essere impostato su uno dei valori seguenti:



| Contrassegno                                 | Significato                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamento predefinito.                                                                                                                                                                           |
| \_ \_ immagine singola della finestra di dialogo del dispositivo WIA \_ \_   | Limitare la selezione delle immagini a una singola immagine nella finestra di dialogo acquisizione immagine del dispositivo.                                                                                                      |
| \_finestra di dialogo del dispositivo WIA usare l' \_ \_ \_ \_ interfaccia utente comune | Utilizzare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore. Se l'interfaccia utente del sistema non è disponibile, viene utilizzata l'interfaccia utente del fornitore. Se nessuna delle due interfacce è disponibile, la funzione restituisce E \_ NOTIMPL. |



 

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

**bstrFilename**
</dt> <dd>

Tipo: **BSTR**

</dd> <dd>

Specifica il modello di nome file da utilizzare per i file trasferiti dagli elementi WIA alla cartella di destinazione indicata da **bstrFolderName**. È possibile creare un numero arbitrario di nomi file univoci aggiungendo caratteri aggiuntivi al modello di nome file.

</dd> <dt>

**lNumFiles**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Riceve il numero di stringhe scritte nella matrice **pbstrFilePaths** .

</dd> <dt>

**pbstrFilePaths**
</dt> <dd>

Tipo: **BSTR \** _

</dd> <dd>

Puntatore a una matrice di puntatori BSTR. Ogni elemento della matrice punta a un BSTR che contiene il nome di destinazione di un file che è stato trasferito correttamente nella cartella identificata da bstrFolderName. Il metodo deve allocare lo spazio di archiviazione per il membro.

</dd> <dt>

_ *ppWiaItem**
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

</dd> <dd>

Puntatore all'interfaccia [_ *IWiaItem2* *](-wia-iwiaitem2.md) dell'elemento WIA che trasferisce i dati al file o ai file denominati nella matrice **pbstrFilePaths** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




