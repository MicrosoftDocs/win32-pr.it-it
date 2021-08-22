---
description: Il provider SNMP usa i qualificatori di proprietà CIM seguenti durante il mapping delle definizioni di oggetto MIB alle definizioni di classe CIM.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: Qualificatori di proprietà CIM per oggetti MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2fd45f250b603fcea97040a35faf43f6343311094e97a52ca06823e99bfcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131713"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>Qualificatori di proprietà CIM per oggetti MIB

Il provider SNMP usa i qualificatori di proprietà CIM seguenti durante il mapping delle definizioni di oggetto MIB alle definizioni di classe CIM. È necessario che sia presente un qualificatore obbligatorio per il provider SNMP per risolvere completamente un oggetto MIB. Se non si definisce un qualificatore obbligatorio, viene restituito un errore. Se si specifica un valore di qualificatore non valido, viene restituito anche un errore.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 



| Qualifier                          | Descrizione                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BITS**                           | **string** Obbligatorio se il **qualificatore Textual \_ Convention** non è uguale a BITS.<br/> Valori enumerati per la definizione del sottotipo di un bit.<br/>                                        |
| **Cimtype**                        | **string** Obbligatorio<br/> Rappresentazione testuale CIM che formatta un valore del protocollo CIM sottostante.<br/>                                                                                    |
| **Valore di defval**                         | **string** Opzionale<br/> Valore predefinito dell'oggetto.<br/>                                                                                                                                       |
| **Descrizione**                    | **string** Opzionale<br/> Descrizione dell'oggetto.<br/>                                                                                                                                    |
| **Suggerimento \_ per la visualizzazione**                  | **string** Opzionale<br/> Modalità di visualizzazione dei dati dell'oggetto a un utente.<br/>                                                                                                    |
| **Encoding**                       | **string** Opzionale<br/> Tipo SNMP usato per la codifica dei frame del protocollo SNMPv1 e SNMPv2C.<br/>                                                                                              |
| **Enumerazione**                    | **string** Obbligatorio se il **qualificatore Textual \_ Convention** non è uguale a ENUMERATEDINTEGER.<br/> Valori enumerati per una definizione di sottotipo integer enumerato.<br/>                  |
| **Lunghezza \_ fissa**                  | **uint32** Opzionale<br/> Valore a lunghezza fissa.<br/>                                                                                                                                           |
| [**Chiave**](standard-qualifiers.md) | **Bool** Opzionale<br/> Proprietà chiave di una definizione di classe.<br/>                                                                                                                             |
| **Ordine \_ delle chiavi**                     | **uint32** Facoltativo, a meno [**che non sia**](standard-qualifiers.md) specificato Key.<br/> Ordine della proprietà chiave nella definizione della classe.<br/>                                                   |
| **Nome**                           | **string** Obbligatorio<br/> Nome implicito della proprietà. Si noti che questo qualificatore non è definito in modo esplicito.<br/>                                                                           |
| **Identificatore \_ di oggetto**             | **string** Obbligatorio<br/> Identificatore dell'oggetto MIB dell'oggetto.<br/>                                                                                                                              |
| **Sintassi \_ degli oggetti**                 | **string** Opzionale<br/> Definizione del tipo denominato dell'oggetto.<br/>                                                                                                                               |
| **Lettura**                           | **Bool** Facoltativo (è necessario specificare **almeno una di lettura** **o** scrittura)<br/> Concede l'accesso in lettura all'oggetto .<br/>                                                                     |
| **Riferimento**                      | **string** Opzionale<br/> Fa riferimento a un altro documento che contiene altre informazioni sull'oggetto.<br/>                                                                                   |
| **Status**                         | **string** Opzionale<br/> Indica se l'oggetto deve essere supportato.<br/>                                                                                                               |
| **Convenzione \_ testuale**            | **string** Obbligatorio<br/> Rappresentazione testuale della clausola SYNTAX della macro [OBJECT-TYPE](object-type-macro.md) MIB.<br/>                                                           |
| **Unità**                          | **string** Opzionale<br/> Definizione precisa di ciò che l'oggetto rappresenta.<br/>                                                                                                             |
| **Lunghezza \_ variabile**               | **string** Opzionale<br/> Valori minimo, massimo e a lunghezza fissa associati alla definizione del tipo dell'oggetto.<br/>                                                                       |
| **Valore \_ variabile**                | **string** Opzionale<br/> Valori con intervallo e fissi associati alla definizione del tipo dell'oggetto.<br/>                                                                                         |
| **Chiave \_ virtuale**                   | **Bool** Opzionale<br/> Indica che il valore della proprietà deve essere basato sul superset di informazioni sull'istanza associato a tutti gli oggetti MIB accessibili nella definizione della classe.<br/> |
| **Scrittura**                          | **Bool** Facoltativo (è necessario specificare **almeno una di lettura** **o** scrittura)<br/> Concede l'accesso in scrittura all'oggetto .<br/>                                                                    |



 

 

 




