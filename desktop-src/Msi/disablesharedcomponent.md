---
description: Se questo criterio di sistema per computer è impostato su 1, nessun pacchetto nel sistema ottiene la funzionalità del componente condiviso abilitata dall'attributo msidbComponentAttributesShared nella tabella dei componenti.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527037"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Se questo [criterio di sistema](system-policy.md) per computer è impostato su 1, nessun pacchetto nel sistema ottiene la funzionalità del componente condiviso abilitata dall'attributo **msidbComponentAttributesShared** nella [tabella dei componenti](component-table.md). Il valore predefinito è 0, che consente la funzionalità del componente condiviso per i componenti contrassegnati con **msidbComponentAttributesShared** in tutti i pacchetti.

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Questa funzione è disponibile a partire da Windows Installer 4,5.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



