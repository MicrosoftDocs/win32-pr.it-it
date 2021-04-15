---
description: Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Struttura DEVICEDIALOGDATA (Wiadefd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529155"
---
# <a name="devicedialogdata-structure"></a>Struttura DEVICEDIALOGDATA

Definisce i dati necessari per chiamare una finestra di dialogo del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a>Members

<dl> <dt>

**cbSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Specifica la dimensione in byte della struttura.

</dd> <dt>

**hwndParent**
</dt> <dd>

Tipo: **HWND**

</dd> <dd>

Specifica l'handle per la finestra padre della finestra di dialogo.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _

</dd> <dd>

Punta a un'interfaccia [_ *IWiaItem* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.

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

**lIntent**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Specifica il tipo di dati che l'immagine deve rappresentare. Per un elenco di valori per finalità immagine, vedere [**costanti per finalità di immagine**](-wia-imageintentconstants.md).

</dd> <dt>

**lItemCount**
</dt> <dd>

Tipo: **Long**

</dd> <dd>

Riceve il numero di elementi nella matrice indicata dal parametro **ppWiaItem** .

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Riceve l'indirizzo di una matrice di puntatori alle interfacce [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadefd. h</dt> </dl> |



 

 




