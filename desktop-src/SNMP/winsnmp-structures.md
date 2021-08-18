---
title: Strutture WinSNMP
description: Le funzioni dell'API WinSNMP usano le strutture seguenti.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- Strutture WinSNMP SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b409b6d12063ebd3feb9c663f2d607bc5ceead0462b2945334f1e7e691c9be63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142754"
---
# <a name="winsnmp-structures"></a>Strutture WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Le funzioni dell'API WinSNMP usano le strutture seguenti.



| Struttura                                  | Descrizione                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contiene un intero senza segno a 64 bit che rappresenta un contatore.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contiene un puntatore a una stringa di ottetti SNMP di lunghezza variabile.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contiene un puntatore a una matrice a lunghezza variabile dei sottoidentificatori associati a un oggetto denominato specificato. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Rappresenta il valore associato a un nome di variabile in una voce di associazione di variabili.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contiene informazioni sull'implementazione Microsoft di WinSNMP.                                                    |



 

 

 