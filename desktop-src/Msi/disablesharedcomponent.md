---
description: Se questo criterio di sistema per computer è impostato su 1, nessun pacchetto nel sistema ottiene la funzionalità del componente condiviso abilitata dall'attributo msidbComponentAttributesShared nella tabella Component.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7576406e14b0f9ac48a26735b984302c2d765b784484022a85ec50244ee8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143102"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Se questo criterio di [sistema](system-policy.md) per computer è impostato su 1, nessun pacchetto nel sistema ottiene la funzionalità del componente condiviso abilitata dall'attributo **msidbComponentAttributesShared** nella [tabella Component](component-table.md). Il valore predefinito è 0, che abilita la funzionalità dei componenti condivisi per i componenti contrassegnati con **msidbComponentAttributesShared** in tutti i pacchetti.

**[Windows Installer 4.0 e versioni precedenti:](not-supported-in-windows-installer-4-0.md)** Non supportato. Questa funzione è disponibile a partire da Windows Installer 4.5.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Criteri \_ software del** \\ **computer** \\ **locale Programma** di installazione \\  \\ **Windows** \\ **Microsoft**

## <a name="data-type"></a>Tipo di dati

**REG \_ DWORD**

 

 



