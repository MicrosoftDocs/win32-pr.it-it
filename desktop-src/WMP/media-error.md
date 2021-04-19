---
title: Media. errore
description: La proprietà Error recupera un oggetto ErrorItem se l'elemento multimediale presenta una condizione di errore.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Media. Error Media Player Windows
topic_type:
- apiref
api_name:
- Media.error
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5845252c817a424b0cbe414612fde47ed8b57328
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326724"
---
# <a name="mediaerror"></a>Media. errore

La proprietà **Error** recupera un oggetto **ErrorItem** se l'elemento multimediale presenta una condizione di errore.

## <a name="syntax"></a>Sintassi

*Player*. *currentMedia*. **errore**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un oggetto **ErrorItem** di sola lettura.

## <a name="remarks"></a>Commenti

Se non è possibile riprodurre l'elemento multimediale, questa proprietà recupera un oggetto **ErrorItem** che contiene informazioni sul problema rilevato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Oggetto multimediale**](media-object.md)
</dt> </dl>

 

 





