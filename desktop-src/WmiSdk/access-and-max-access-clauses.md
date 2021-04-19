---
description: Ogni definizione di oggetto MIB contiene una clausola ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) che definisce i diritti di accesso all'oggetto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Clausole ACCESS e MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315253"
---
# <a name="access-and-max-access-clauses"></a>Clausole ACCESS e MAX-ACCESS

Ogni definizione di oggetto MIB contiene una clausola ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) che definisce i diritti di accesso all'oggetto.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Nella tabella seguente viene elencato il mapping della clausola SNMPv1 ACCESS.



| Clausola di accesso MIB | Qualificatore CIM       |
|-------------------|---------------------|
| Sola lettura         | **Lettura**            |
| lettura/scrittura        | **Lettura**, **scrittura** |
| sola scrittura        | **Scrittura**           |
| non accessibile    | **Non \_ accessibile** |



 

La tabella seguente elenca il mapping della clausola SNMPv2C MAX-ACCESS.



| Clausola di accesso MIB     | Qualificatore CIM       |
|-----------------------|---------------------|
| Sola lettura             | **Lettura**            |
| lettura/scrittura            | **Lettura**, **scrittura** |
| lettura-creazione           | **Lettura**            |
| accessibilità per notifica | **Non \_ accessibile** |
| non accessibile        | **Non \_ accessibile** |



 

Quando un oggetto MIB viene mappato a non accessibile e non è una proprietà con chiave della classe, non esiste alcun mapping dell'oggetto MIB stesso.

 

 



