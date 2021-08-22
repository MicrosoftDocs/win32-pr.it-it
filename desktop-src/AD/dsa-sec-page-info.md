---
title: DSA_SEC_PAGE_INFO struttura
description: Usato con i messaggi WM ADSPROP SHEET CREATE e WM DSA SHEET CREATE NOTIFY per definire una finestra delle proprietà secondaria in uno \_ \_ \_ \_ \_ \_ \_ snap-in MMC di Active Directory.
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO structure Active Directory
- PDSA_SEC_PAGE_INFO puntatore alla struttura active directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26fa3dcfb983de8e1052b319bac7c3a594e256b594847c32b553353e6caee17d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695649"
---
# <a name="dsa_sec_page_info-structure"></a>Struttura DSA \_ SEC \_ PAGE \_ INFO

La **struttura DSA \_ SEC PAGE \_ \_ INFO** viene usata con i messaggi [**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md) e [**WM \_ DSA \_ SHEET CREATE \_ \_ NOTIFY**](wm-dsa-sheet-create-notify.md) per definire una finestra delle proprietà secondaria in uno snap-in MMC di Active Directory.

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

Contiene l'handle di finestra dell'elemento padre della finestra delle proprietà secondaria.

</dd> <dt>

**offsetTitle**
</dt> <dd>

Contiene l'offset, in byte, dall'inizio della struttura **DSA \_ SEC \_ PAGE \_ INFO** a una stringa Unicode con terminazione NULL che contiene il titolo della finestra delle proprietà secondaria.

</dd> <dt>

**dsObjectNames**
</dt> <dd>

Contiene una [**struttura DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) che definisce la finestra delle proprietà secondaria. È possibile creare una sola finestra delle proprietà secondaria alla volta, quindi la struttura **DSOBJECTNAMES** può contenere solo una [**struttura DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**NOTIFICA \_ DI CREAZIONE FOGLIO WM DSA \_ \_ \_**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





