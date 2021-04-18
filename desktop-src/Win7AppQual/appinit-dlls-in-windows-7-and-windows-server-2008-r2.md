---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318896"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>\_Dll di AppInit in Windows 7 e Windows Server 2008 R2

## <a name="platform"></a>Piattaforma

**Client** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

AppInit \_ dll è un meccanismo che consente di caricare un elenco arbitrario di dll in ogni processo in modalità utente nel sistema. Microsoft sta modificando la funzionalità dll di AppInit in Windows 7 e Windows Server 2008 R2 per aggiungere un nuovo requisito per la firma del codice. Ciò consentirà di migliorare l'affidabilità e le prestazioni del sistema, nonché di migliorare la visibilità dell'origine del software.

## <a name="configuration"></a>Configurazione

I valori archiviati in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows Key nel registro di sistema determinano il comportamento dell' \_ infrastruttura di DLL AppInit. La tabella seguente descrive i valori del registro di sistema:



<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
<th>Valori di esempio</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">Abilita o Disabilita globalmente AppInit_DLLs. $ {REMOVE} $<br />
</td>
<td>0x0: AppInit_DLLs sono disabilitati.</td>
</tr>
<tr class="even">
<td>0x1: AppInit_DLLs sono abilitati.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Spazio o elenco delimitato da virgole di dll da caricare. Il percorso completo della DLL deve essere specificato utilizzando nomi brevi.</td>
<td>C:\ PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD) $ {REMOVE} $<br />
</td>
<td rowspan="2">Carica solo le dll con firma codice. $ {REMOVE} $<br />
</td>
<td>0x0: carica qualsiasi dll.</td>
</tr>
<tr class="odd">
<td>0x1: carica solo le dll con firma di codice.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Tutte le DLL caricate dall'infrastruttura di \_ DLL AppInit devono essere firmate dal codice. Per motivi di compatibilità delle applicazioni, il sistema operativo Windows 7 caricherà tutte le DLL AppInit. Tuttavia, Microsoft consiglia a tutti gli sviluppatori di applicazioni di firmare il codice delle proprie DLL per migliorare l'affidabilità di Windows e prepararsi per l'imposizione della firma del codice nelle versioni successive di Windows. La \_ chiave del registro di sistema dll RequireSignedAppInit controlla questo comportamento e il relativo valore in Windows 7 è impostato su 0 per impostazione predefinita.

**Windows Server 2008 R2**

Tutte le DLL caricate dall' \_ infrastruttura dll di AppInit devono avere la firma del codice. La \_ chiave del registro di sistema dll RequireSignedAppInit controlla questo comportamento e il relativo valore in Windows Server 2008 R2 è impostato su 1 per impostazione predefinita.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[Dll di AppInit in Windows 7 e Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
