---
title: Errori comuni (AD DS)
description: La tabella seguente contiene un elenco di errori comuni che possono verificarsi in base all'ambito del gruppo nidificato.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Errori comuni AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "104472179"
---
# <a name="common-errors-ad-ds"></a>Errori comuni (AD DS)

La tabella seguente contiene un elenco di errori comuni che possono verificarsi in base all'ambito del gruppo nidificato.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>HRESULT</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x8007001F</td>
<td>Errore generale. Questo errore si verifica se si tenta di eseguire le operazioni seguenti:
<ul>
<li>Aggiungere un gruppo locale di dominio a un gruppo globale o universale o a un gruppo locale di dominio in un altro dominio. I gruppi locali di dominio possono essere aggiunti solo come membri ad altri gruppi locali di dominio nello stesso dominio.</li>
<li>Aggiungere un gruppo universale a un gruppo globale. I gruppi universali possono essere aggiunti a gruppi locali universali e di dominio, ma non a gruppi globali.</li>
</ul></td>
</tr>
<tr class="even">
<td>0x8007202F</td>
<td><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>. Questo errore si verifica se si tenta di aggiungere un gruppo di sicurezza a un altro gruppo in un dominio in esecuzione in modalità mista. Non è possibile nidificare i gruppi di sicurezza in modalità mista. i gruppi di sicurezza possono essere annidati solo in modalità nativa.</td>
</tr>
</tbody>
</table>



 

 

 




