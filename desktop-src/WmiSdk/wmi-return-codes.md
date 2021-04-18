---
description: In questa sezione viene fornito un elenco dei codici restituiti WMI, delle costanti simboliche, dei valori letterali e delle descrizioni. Questi codici possono essere restituiti da script, applicazioni C++ o comandi WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Codici restituiti WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309746"
---
# <a name="wmi-return-codes"></a>Codici restituiti WMI

In questa sezione viene fornito un elenco dei codici restituiti WMI, delle costanti simboliche, dei valori letterali e delle descrizioni. Questi codici possono essere restituiti da script, applicazioni C++ o comandi [**wmic**](wmic.md) .

Se si verifica un errore, WMI restituisce uno dei codici di errore seguenti come valore a 32 bit in cui i due bit più significativi indicano il codice di gravità del messaggio.

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
> Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI. Gli errori possono provenire in altre parti del sistema operativo e emergono come errori tramite WMI. In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.
>
> Per ottenere ulteriori informazioni sull'origine del problema, è possibile scaricare ed eseguire lo strumento da riga di comando [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostica. Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo. Il report contribuisce inoltre ai servizi di supporto tecnico Microsoft. È possibile scaricare il Utilità di diagnosi di WMI [qui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

-   [**Costanti di errore WMI**](wmi-error-constants.md)
-   [**Costanti non di errore WMI**](wmi-non-error-constants.md)

 

 



