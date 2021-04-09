---
description: Il riferimento di scripting WMI contiene le definizioni per l'API di scripting WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API di scripting per WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880442"
---
# <a name="scripting-api-for-wmi"></a>API di scripting per WMI

Il riferimento di scripting WMI contiene le definizioni per l'API di scripting WMI. Usare questa API se si scrivono applicazioni con Microsoft Visual Basic, Visual Basic, Applications Edition, Visual Basic Scripting Edition (VBScript) o qualsiasi altro linguaggio di script che supporta le tecnologie di scripting.

> [!Note]  
> PowerShell è inoltre disponibile per lo scripting con WMI. Il cmdlet Get-WMI e i tre acceleratori di tipo ( \[ WMI \] , \[ WMIClass \] e \[ WMISEARCHER \] ) abilitano l'accesso amministrativo di base a WMI. Per altre informazioni, vedere Creazione di [script con Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Gli oggetti di scripting WMI, ad eccezione di [**SWbemDateTime**](swbemdatetime.md) , non sono contrassegnati come sicuri per lo scripting per gli script in esecuzione sulle pagine HTML in Internet Explorer. Pertanto, a meno che il livello di sicurezza in Internet Explorer non venga ridotto, lo script avrà esito negativo. **SWbemDateTime** è contrassegnato come Safe per l'inizializzazione e lo scripting. Tuttavia, utilizzare tutti gli oggetti di scripting WMI nelle chiamate **GetObject** e **CreateObject** sul codice sul lato server in Active Server Pages (ASP).

-   [Modello a oggetti API di scripting](scripting-api-object-model.md)
-   [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md)
-   [Oggetti API di scripting](scripting-api-objects.md)
-   [Esecuzione di script di costanti API](scripting-api-constants.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dt>

[Codici restituiti WMI](wmi-return-codes.md)
</dt> </dl>

 

 



