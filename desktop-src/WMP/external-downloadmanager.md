---
title: External.DownloadManager
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. La proprietà DownloadManager recupera l'oggetto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- External.DownloadManager Windows Media Player
topic_type:
- apiref
api_name:
- External.DownloadManager
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d828435c43f57406e637312245b2bb3ae3e7c35510c9b2daf478a7fec39b599
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649211"
---
# <a name="externaldownloadmanager"></a>External.DownloadManager

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

La **proprietà DownloadManager** recupera l'oggetto **DownloadManager.**

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **DownloadManager di sola** lettura.

## <a name="remarks"></a>Commenti

In Windows Media Player 10 o versioni successive, la proprietà e l'oggetto **DownloadManager** sono accessibili solo dai riquadri attività del servizio negozio online. Non è possibile usare **DownloadManager** da altre funzionalità in cui è disponibile l'oggetto **External,** ad esempio HTMLView, la visualizzazione Info Center e le informazioni sugli album.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 2**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





