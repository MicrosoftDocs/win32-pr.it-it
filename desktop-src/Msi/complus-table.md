---
description: La tabella ComPlus contiene le informazioni necessarie per installare le applicazioni COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabella ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318294"
---
# <a name="complus-table"></a>Tabella ComPlus

La tabella ComPlus contiene le informazioni necessarie per installare le applicazioni COM+.

La tabella ComPlus include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| ExpType     | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md). Si tratta del componente che contiene l'applicazione COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Flag di esportazione utilizzati durante la generazione del file con estensione msi. Per ulteriori informazioni, vedere la documentazione COM+ in Microsoft Windows Software Development Kit (SDK).

</dd> </dl>

## <a name="remarks"></a>Commenti

Vedere l'azione [RegisterComPlus](registercomplus-action.md) e l' [azione UnregisterComPlus](unregistercomplus-action.md).

Vedere [installazione di un'applicazione com+ con la Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



