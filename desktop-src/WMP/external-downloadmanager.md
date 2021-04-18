---
title: External. DownloadManager
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà DownloadManager recupera l'oggetto DownloadManager.
ms.assetid: 9fec7175-611e-4e7e-8978-132e6f86329a
keywords:
- Media Player di Windows External. DownloadManager
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
ms.openlocfilehash: f55e6371f5c8d1e5dfcb17762340a82e8d921c17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328887"
---
# <a name="externaldownloadmanager"></a>External. DownloadManager

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **downloadmanager** recupera l'oggetto **downloadmanager** .

``` syntax
window.external.DownloadManager
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **downloadmanager** di sola lettura.

## <a name="remarks"></a>Commenti

In Windows Media Player 10 o versioni successive, la proprietà e l'oggetto **downloadmanager** sono accessibili solo dai riquadri attività del servizio di archiviazione online. Non è possibile usare **downloadmanager** da altre funzionalità in cui l'oggetto **esterno** è disponibile, ad esempio HtmlView, visualizzazione centro informazioni e informazioni sugli album.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 2 online**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





