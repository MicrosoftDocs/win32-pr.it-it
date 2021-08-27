---
description: In questa sezione viene fornito un elenco di codici restituiti WMI, costanti simboliche, valori letterali e descrizioni. Questi codici possono essere restituiti da script, applicazioni C++ o comandi Wmic.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Codici restituiti WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1454c8efc45085e88f78358346679b5cdcf3d05093318845912d7d5a913d8ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995381"
---
# <a name="wmi-return-codes"></a>Codici restituiti WMI

In questa sezione viene fornito un elenco di codici restituiti WMI, costanti simboliche, valori letterali e descrizioni. Questi codici possono essere restituiti da script, applicazioni C++ o [**comandi Wmic.**](wmic.md)

Se si verifica un errore, WMI restituisce uno dei codici di errore seguenti come valore a 32 bit in cui i due bit più elevati indicano il codice di gravità del messaggio.

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Operazione riuscita

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Informativo

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

Avviso

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

Errore

</dd> </dl>

> [!Note]
>
> Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI. Gli errori possono avere origine in altre parti del sistema operativo e emergono come errori tramite WMI. In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.
>
> Per ottenere altre informazioni sull'origine del problema, è possibile scaricare ed eseguire lo Utilità di diagnosi di WMI [della](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) riga di comando di diagnostica. Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo. Il report aiuta anche i servizi di supporto Tecnico Microsoft a fornire assistenza. È possibile scaricare il Utilità di diagnosi di WMI [qui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

-   [**Costanti di errore WMI**](wmi-error-constants.md)
-   [**Costanti WMI non di errore**](wmi-non-error-constants.md)

 

 



