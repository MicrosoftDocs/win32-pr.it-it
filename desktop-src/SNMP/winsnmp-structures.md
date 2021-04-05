---
title: Strutture WinSNMP
description: Le funzioni API WinSNMP utilizzano le strutture seguenti.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- WinSNMP strutture SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872717"
---
# <a name="winsnmp-structures"></a>Strutture WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Le funzioni API WinSNMP utilizzano le strutture seguenti.



| Struttura                                  | Descrizione                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contiene un valore Unsigned Integer a 64 bit che rappresenta un contatore.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contiene un puntatore a una stringa di ottetto SNMP di lunghezza variabile.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contiene un puntatore a una matrice di lunghezza variabile dei sottoidentificatori associati a un oggetto denominato specificato. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Rappresenta il valore associato a un nome di variabile in una voce di associazione variabile.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contiene informazioni sull'implementazione Microsoft di WinSNMP.                                                    |



 

 

 