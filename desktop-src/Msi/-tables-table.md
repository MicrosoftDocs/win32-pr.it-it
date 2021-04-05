---
description: La \_ tabella Tables è una tabella di sistema di sola lettura in cui sono elencate tutte le tabelle del database. Eseguire una query su questa tabella per verificare se esiste una tabella.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Tabella _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881189"
---
# <a name="_tables-table"></a>\_Tabella tabelle

La \_ tabella Tables è una tabella di sistema di sola lettura in cui sono elencate tutte le tabelle del database. Eseguire una query su questa tabella per verificare se esiste una tabella.

La \_ tabella tables contiene la seguente colonna.



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

Poiché la \_ tabella Tables è una tabella di sistema che non può essere modificata tramite query SQL, non è possibile ottenere le chiavi primarie con la funzione [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) o la [**Proprietà PrimaryKeys**](database-primarykeys.md).

 

 



