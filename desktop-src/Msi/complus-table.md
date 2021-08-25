---
description: La tabella Complus contiene le informazioni necessarie per installare le applicazioni COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabella Complus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77885688226689e5d81e074b1a9a28ef3801aaeba5febf51165377ac9ad9e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144972"
---
# <a name="complus-table"></a>Tabella Complus

La tabella Complus contiene le informazioni necessarie per installare le applicazioni COM+.

La tabella Complus include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| ExpType     | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Component](component-table.md). Si tratta del componente che contiene l'applicazione COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Flag di esportazione usati durante la generazione del file .msi file. Per altre informazioni, vedere la documentazione di COM+ in Microsoft Windows Software Development Kit (SDK).

</dd> </dl>

## <a name="remarks"></a>Commenti

Vedere [l'azione RegisterComPlus e](registercomplus-action.md) [l'azione UnregisterComPlus](unregistercomplus-action.md).

Vedere [Installazione di un'applicazione COM+ con il Windows installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



