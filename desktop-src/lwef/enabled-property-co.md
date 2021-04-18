---
title: Proprietà Enabled (oggetto Command)
description: Proprietà Enabled
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300831"
---
# <a name="enabled-property-command-object"></a>Proprietà Enabled (oggetto Command)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta un valore che indica se il **comando** è abilitato nel menu di scelta rapida del carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_"). Comandi ("_*_Name_*_")._ *  \[  =  *Valore booleano* abilitato\]



| Parte      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Espressione booleana che specifica se il **comando** è abilitato.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Vero**</dt> <dd> Il **comando** è abilitato.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt> <dd> Il **comando** è disabilitato.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se la proprietà [**Enabled**](enabled-property.md) è impostata su **true**, la didascalia degli oggetti [**comando**](/windows/desktop/lwef/the-command-object) viene visualizzata come testo normale nel menu popup del carattere quando l'applicazione client è di tipo input-attivo. Se la proprietà **Enabled** è **false**, la didascalia viene visualizzata come testo non disponibile (disabilitato). Non è inoltre possibile accedere a un **comando** disabilitato per l'input vocale.

 

