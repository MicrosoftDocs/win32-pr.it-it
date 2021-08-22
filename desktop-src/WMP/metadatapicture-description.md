---
title: MetadataPicture.description
description: La proprietà description recupera una descrizione dell'immagine dei metadati.
ms.assetid: 7a07a8a0-d50a-4951-95a8-c1285a1be737
keywords:
- MetadataPicture.description Windows Media Player
topic_type:
- apiref
api_name:
- MetadataPicture.description
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32868fbf276b5892bb5444093bf683920233483aa9756a5cc4ea63b490c0d023
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508361"
---
# <a name="metadatapicturedescription"></a>MetadataPicture.description

La **proprietà description** recupera una descrizione dell'immagine dei metadati.

## <a name="syntax"></a>Sintassi

*lettore*. *currentMedia*. **getItemInfoByType**( *name*, *language*, *index*). **description**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**

## <a name="remarks"></a>Commenti

Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria. Per altre informazioni, vedere [Accesso alla libreria](library-access.md).

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto MetadataPicture**](metadatapicture-object.md)
</dt> <dt>

[**Impostazioni.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





