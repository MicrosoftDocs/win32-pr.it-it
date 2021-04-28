---
description: AppInit_DLLs in Windows 7 e Windows Server 2008 R2
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820fcb9840bbec139ff78f3c6cc082b2dca4eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088709"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a>DLL AppInit \_ in Windows 7 e Windows Server 2008 R2

## <a name="platform"></a>Piattaforma

**Client** - Windows 7  
**Server** - Windows Server 2008 R2  









## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

Le DLL AppInit sono un meccanismo che consente il caricamento di un elenco arbitrario di DLL in ogni processo in modalità \_ utente nel sistema. Microsoft sta modificando la funzionalità delle DLL AppInit in Windows 7 e Windows Server 2008 R2 per aggiungere un nuovo requisito di firma del codice. Ciò consente di migliorare l'affidabilità e le prestazioni del sistema, nonché di migliorare la visibilità sull'origine del software.

## <a name="configuration"></a>Configurazione

I valori archiviati nella chiave HKEY LOCAL MACHINE SOFTWARE Microsoft Windows NT currentVersion di Windows nel Registro di sistema determinano il comportamento dell'infrastruttura \_ \_ delle DLL \\ \\ \\ \\ \\ \_ AppInit. La tabella seguente descrive questi valori del Registro di sistema:



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
<td rowspan="2">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$<br />
</td>
<td rowspan="2">Abilita o disabilita a livello globale AppInit_DLLs.${REMOVE}$<br />
</td>
<td>0x0: AppInit_DLLs disabilitate.</td>
</tr>
<tr class="even">
<td>0x1: AppInit_DLLs abilitate.</td>


</tr>
<tr class="odd">
<td>AppInit_DLLs (REG_SZ)</td>
<td>Elenco delimitato da spazi o virgole di DLL da caricare. Il percorso completo della DLL deve essere specificato usando nomi brevi.</td>
<td>C:\ PROGRA~1\WID288~1\MICROS~1.DLL</td>
</tr>
<tr class="even">
<td rowspan="2">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$<br />
</td>
<td rowspan="2">Caricare solo LE DLL firmate dal codice.${REMOVE}$<br />
</td>
<td>0x0: caricare le DLL.</td>
</tr>
<tr class="odd">
<td>0x1: caricare solo LE DLL firmate dal codice.</td>


</tr>
</tbody>
</table>



 

**Windows 7**

Tutte le DLL caricate dall'infrastruttura delle DLL AppInit devono \_ essere firmate dal codice. Nell'interesse della compatibilità delle applicazioni, il sistema operativo Windows 7 carica tutte le DLL AppInit. Tuttavia, Microsoft consiglia a tutti gli sviluppatori di applicazioni di firmare il codice delle DLL per migliorare l'affidabilità di Windows e prepararsi per l'applicazione della firma del codice nelle versioni future di Windows. La chiave del Registro di sistema RequireSignedAppInit controlla questo comportamento e il relativo valore in Windows 7 è impostato \_ su 0 per impostazione predefinita.

**Windows Server 2008 R2**

Tutte le DLL caricate dall'infrastruttura delle DLL AppInit \_ devono essere firmate con codice. La chiave del Registro di sistema RequireSignedAppInit controlla questo comportamento e il relativo valore \_ in Windows Server 2008 R2 è impostato su 1 per impostazione predefinita.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

<dl>

[DLL AppInit in Windows 7 e Windows Server 2008 R2](/windows-hardware/drivers/install/)  
</dl>

 

 
