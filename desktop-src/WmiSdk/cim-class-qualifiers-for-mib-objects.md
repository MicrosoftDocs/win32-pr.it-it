---
description: Il provider SNMP usa i qualificatori di classe CIM seguenti per eseguire il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Qualificatori di classe CIM per oggetti MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233251"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a>Qualificatori di classe CIM per oggetti MIB

Il provider SNMP usa i qualificatori di classe CIM seguenti per eseguire il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM. Per il provider SNMP per la risoluzione completa di un oggetto gruppo, è necessario che sia presente un qualificatore obbligatorio. La mancata definizione di un qualificatore obbligatorio restituisce un errore. Se si specifica un valore qualificatore non valido, viene restituito anche un errore.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 



| Qualifier           | Descrizione                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Descrizione**     | **stringa** di Opzionale<br/> Descrizione della classe.<br/>                                                                      |
| **ObjectId del gruppo \_** | **stringa** di Obbligatoria, se la classe è per il provider di classi SNMP.<br/> Identificatore di oggetto della raccolta fabbricata.<br/> |
| **Importazioni di moduli \_** | **stringa** di Opzionale<br/> Elenco delimitato da virgole di nomi di moduli MIB usati per risolvere le importazioni.<br/>                              |
| **Nome del modulo \_**    | **stringa** di Opzionale<br/> Nome identità di un modulo MIB.<br/>                                                                 |
| **Riferimento**       | **stringa** di Opzionale<br/> Fa riferimento a un altro documento che contiene ulteriori informazioni sulla classe.<br/>                     |
| **Singleton**       | **Bool** Obbligatorio per le classi mappate da raccolte scalari.<br/> Indica una classe che può avere una sola istanza.<br/>  |



 

 

 




