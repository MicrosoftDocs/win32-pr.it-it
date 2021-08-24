---
description: Il riferimento agli script WMI contiene le definizioni per l'API di scripting WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API di scripting per WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35045aa8528c5a3c27475fff753478bd2202d9137cec6b019039aac52775f70a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640541"
---
# <a name="scripting-api-for-wmi"></a>API di scripting per WMI

Il riferimento agli script WMI contiene le definizioni per l'API di scripting WMI. Usare questa API se si scrivono applicazioni con Microsoft Visual Basic, Visual Basic, Applications Edition, Visual Basic Scripting Edition (VBScript) o qualsiasi altro linguaggio di scripting che supporta tecnologie di scripting attive.

> [!Note]  
> PowerShell è disponibile anche per lo scripting con WMI. Il cmdlet Get-WMI e i tre acceleratori di tipo ( \[ wmi \] , wmiclass e wmisearcher ) consentono l'accesso \[ \] \[ \] amministrativo di base a WMI. Per altre informazioni, vedere [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Gli oggetti di scripting WMI, ad eccezione [**di SWbemDateTime,**](swbemdatetime.md) non sono contrassegnati come sicuri per gli script in esecuzione nelle pagine HTML Internet Explorer. Pertanto, a meno che il livello di sicurezza Internet Explorer venga abbassato, lo script avrà esito negativo. **SWbemDateTime** è contrassegnato come sicuro per l'inizializzazione e lo scripting. Tuttavia, usare tutti gli oggetti di scripting WMI nelle chiamate **GetObject** e **CreateObject** sul codice lato server in Active Server Pages (ASP).

-   [Modello a oggetti dell'API di scripting](scripting-api-object-model.md)
-   [Convenzioni dei documenti per l'API scripting](document-conventions-for-the-scripting-api.md)
-   [Scripting di oggetti API](scripting-api-objects.md)
-   [Costanti dell'API di scripting](scripting-api-constants.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su WMI](wmi-reference.md)
</dt> <dt>

[Codici restituiti WMI](wmi-return-codes.md)
</dt> </dl>

 

 



