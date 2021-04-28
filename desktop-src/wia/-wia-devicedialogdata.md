---
description: 'Struttura DEVICEDIALOGDATA: definisce i dati necessari per chiamare un dialogo del dispositivo.'
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: Struttura DEVICEDIALOGDATA (Wiadefd.h)
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
ms.openlocfilehash: ad7b08f5396a7a6e9b1f74df3dd409303b2d548d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104269"
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

Specifica le dimensioni della struttura in byte.

</dd> <dt>

**hwndParent**
</dt> <dd>

Tipo: **HWND**

</dd> <dd>

Specifica l'handle per la finestra padre della finestra di dialogo.

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\***

</dd> <dd>

Punta a [**un'interfaccia IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) che rappresenta l'elemento radice valido nell'albero degli elementi dell'applicazione.

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

**lIntent**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Specifica il tipo di dati che l'immagine deve rappresentare. Per un elenco dei valori di finalità dell'immagine, vedere [**Costanti finalità immagine.**](-wia-imageintentconstants.md)

</dd> <dt>

**lItemCount**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Riceve il numero di elementi nella matrice indicata dal **parametro ppWiaItem.**

</dd> <dt>

**ppWiaItem**
</dt> <dd>

Tipo: **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

Riceve l'indirizzo di una matrice di puntatori [**alle interfacce IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wiadefd.h</dt> </dl> |



 

 




