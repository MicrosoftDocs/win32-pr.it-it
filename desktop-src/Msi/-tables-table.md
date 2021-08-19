---
description: La tabella Tables è una tabella di sistema di sola \_ lettura che elenca tutte le tabelle nel database. Eseguire una query su questa tabella per determinare se esiste una tabella.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c251693d89bb23634b222518e98dba270856e672362bcdc9acddd3c0b86c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013319"
---
# <a name="_tables-table"></a>\_Tabella Tabelle

La tabella Tables è una tabella di sistema di sola \_ lettura che elenca tutte le tabelle nel database. Eseguire una query su questa tabella per determinare se esiste una tabella.

La \_ tabella Tabelle include la colonna seguente.



| Colonna | Tipo             | Chiave | Nullable |
|--------|------------------|-----|----------|
| Nome   | [Text](text.md) | S   | N        |



 

## <a name="column"></a>Colonna

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome di una delle tabelle.

</dd> </dl>

## <a name="remarks"></a>Commenti

Poiché la tabella Tables è una tabella di sistema che non può essere modificata tramite query SQL, non è possibile ottenere le chiavi primarie con la funzione \_ [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**proprietà PrimaryKeys**](database-primarykeys.md).

 

 



