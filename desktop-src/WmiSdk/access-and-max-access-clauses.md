---
description: Ogni definizione di oggetto MIB contiene una clausola ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) che definisce i diritti di accesso all'oggetto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Clausole ACCESS e MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985b4bfe968841436cedd352a01a609aac6ba2d725887b6a638ffcd95656935d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120941"
---
# <a name="access-and-max-access-clauses"></a>Clausole ACCESS e MAX-ACCESS

Ogni definizione di oggetto MIB contiene una clausola ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) che definisce i diritti di accesso all'oggetto.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

Nella tabella seguente viene elencato il mapping della clausola ACCESS SNMPv1.



| Clausola ACCESS MIB | Qualificatore CIM       |
|-------------------|---------------------|
| Sola lettura         | **Lettura**            |
| lettura/scrittura        | **Lettura,** **scrittura** |
| sola scrittura        | **Scrittura**           |
| non accessibile    | **Non \_ accessibile** |



 

Nella tabella seguente viene elencato il mapping della clausola SNMPv2C MAX-ACCESS.



| Clausola MIB-ACCESS     | Qualificatore CIM       |
|-----------------------|---------------------|
| Sola lettura             | **Lettura**            |
| lettura/scrittura            | **Lettura,** **scrittura** |
| lettura-creazione           | **Lettura**            |
| accessible-for-notify | **Non \_ accessibile** |
| non accessibile        | **Non \_ accessibile** |



 

Quando un oggetto MIB esegue il mapping a non accessibile e non è una proprietà con chiave della classe , non esiste alcun mapping dell'oggetto MIB stesso.

 

 



