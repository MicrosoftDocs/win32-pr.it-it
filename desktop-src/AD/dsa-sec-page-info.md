---
title: Struttura DSA_SEC_PAGE_INFO
description: Usato con il foglio \_ ADSPROP \_ WM \_ Crea e WM \_ DSA \_ foglio \_ Crea \_ notifica messaggi per definire una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- Struttura DSA_SEC_PAGE_INFO Active Directory
- Puntatore alla struttura PDSA_SEC_PAGE_INFO Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964484"
---
# <a name="dsa_sec_page_info-structure"></a>\_Struttura delle \_ informazioni di pagina di DSA sec \_

La struttura delle **\_ informazioni della \_ pagina \_ DSA sec** viene usata con il foglio [**ADSPROP di WM \_ \_ \_ Crea**](wm-adsprop-sheet-create.md) e il [**\_ foglio DSA WM \_ \_ Crea \_ notifica**](wm-dsa-sheet-create-notify.md) messaggi per definire una finestra delle proprietà secondaria in uno snap-in di MMC Active Directory.

> [!Note]  
> Questa struttura non è definita in un file di intestazione pubblicato. Per usare questa struttura, definirla nel formato esatto illustrato.

 

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**hwndParentSheet**
</dt> <dd>

Contiene l'handle della finestra padre della finestra delle proprietà secondaria.

</dd> <dt>

**offsetTitle**
</dt> <dd>

Contiene l'offset, in byte, dall'inizio della struttura di **\_ informazioni della \_ pagina \_ DSA sec** a una stringa Unicode con terminazione null che contiene il titolo della finestra delle proprietà secondaria.

</dd> <dt>

**dsObjectNames**
</dt> <dd>

Contiene una struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) che definisce la finestra delle proprietà secondaria. È possibile creare una sola finestra delle proprietà secondaria alla volta, quindi la struttura **DSOBJECTNAMES** può contenere solo una struttura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ creazione foglio ADSPROP \_ WM**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**\_ \_ \_ creazione \_ notifica foglio DSA WM**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





