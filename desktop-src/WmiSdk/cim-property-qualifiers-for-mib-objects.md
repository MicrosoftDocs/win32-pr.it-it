---
description: Il provider SNMP usa i qualificatori di proprietà CIM seguenti quando si esegue il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: Qualificatori di proprietà CIM per oggetti MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f2a25edf9c15930202d3c8cf79d3d62b0d1dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233247"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>Qualificatori di proprietà CIM per oggetti MIB

Il provider SNMP usa i qualificatori di proprietà CIM seguenti quando si esegue il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM. Per il provider SNMP è necessario che sia presente un qualificatore obbligatorio per la risoluzione completa di un oggetto MIB. La mancata definizione di un qualificatore obbligatorio restituisce un errore. Se si specifica un valore qualificatore non valido, viene restituito anche un errore.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 



| Qualifier                          | Descrizione                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BITS**                           | **stringa** di Obbligatorio, se il qualificatore della **\_ convenzione testuale** non è uguale a BITS.<br/> Valori enumerati per la definizione del sottotipo di un bit.<br/>                                        |
| **CimType**                        | **stringa** di Obbligatorio<br/> Rappresentazione testuale CIM che formatta un valore del protocollo CIM sottostante.<br/>                                                                                    |
| **DEFVAL**                         | **stringa** di Opzionale<br/> Valore predefinito dell'oggetto.<br/>                                                                                                                                       |
| **Descrizione**                    | **stringa** di Opzionale<br/> Descrizione dell'oggetto.<br/>                                                                                                                                    |
| **Hint per la visualizzazione \_**                  | **stringa** di Opzionale<br/> Modalità di visualizzazione dei dati dell'oggetto da parte di un utente.<br/>                                                                                                    |
| **Encoding**                       | **stringa** di Opzionale<br/> Tipo SNMP usato per la codifica di frame di protocollo SNMPv1 e SNMPv2C.<br/>                                                                                              |
| **Enumerazione**                    | **stringa** di Obbligatorio, se il qualificatore della **\_ convenzione testuale** non è uguale a ENUMERATEDINTEGER.<br/> Valori enumerati per una definizione di sottotipo Integer enumerato.<br/>                  |
| **\_Lunghezza fissa**                  | **UInt32** Opzionale<br/> Valore a lunghezza fissa.<br/>                                                                                                                                           |
| [**Chiave**](standard-qualifiers.md) | **Bool** Opzionale<br/> Proprietà chiave di una definizione di classe.<br/>                                                                                                                             |
| **\_Ordine chiavi**                     | **UInt32** Facoltativo, a meno che non sia specificato [**Key**](standard-qualifiers.md) .<br/> Ordine della proprietà chiave nella definizione della classe.<br/>                                                   |
| **Nome**                           | **stringa** di Obbligatorio<br/> Nome implicito della proprietà. Si noti che questo qualificatore non è definito in modo esplicito.<br/>                                                                           |
| **\_Identificatore oggetto**             | **stringa** di Obbligatorio<br/> Identificatore di oggetto MIB dell'oggetto.<br/>                                                                                                                              |
| **Sintassi dell'oggetto \_**                 | **stringa** di Opzionale<br/> Definizione del tipo denominato dell'oggetto.<br/>                                                                                                                               |
| **Lettura**                           | **Bool** Facoltativo (è necessario specificare almeno uno dei **valori di lettura** o **scrittura** )<br/> Concede l'accesso in lettura all'oggetto.<br/>                                                                     |
| **Riferimento**                      | **stringa** di Opzionale<br/> Fa riferimento a un altro documento che contiene ulteriori informazioni sull'oggetto.<br/>                                                                                   |
| **Status**                         | **stringa** di Opzionale<br/> Indica se l'oggetto deve essere supportato.<br/>                                                                                                               |
| **\_Convenzione testuale**            | **stringa** di Obbligatorio<br/> Rappresentazione testuale della clausola SYNTAX della macro di [tipo oggetto](object-type-macro.md) MIB.<br/>                                                           |
| **Unità**                          | **stringa** di Opzionale<br/> Definizione precisa dell'oggetto rappresentato dall'oggetto.<br/>                                                                                                             |
| **\_Lunghezza variabile**               | **stringa** di Opzionale<br/> Valori minimo, massimo e a lunghezza fissa associati alla definizione di tipo dell'oggetto.<br/>                                                                       |
| **Valore della variabile \_**                | **stringa** di Opzionale<br/> Valori a intervalli e fissi associati alla definizione di tipo dell'oggetto.<br/>                                                                                         |
| **\_Chiave virtuale**                   | **Bool** Opzionale<br/> Indica che il valore della proprietà deve essere basato sul superset delle informazioni sull'istanza associate a tutti gli oggetti MIB accessibili nella definizione della classe.<br/> |
| **Scrittura**                          | **Bool** Facoltativo (è necessario specificare almeno uno dei **valori di lettura** o **scrittura** )<br/> Concede l'accesso in scrittura all'oggetto.<br/>                                                                    |



 

 

 




