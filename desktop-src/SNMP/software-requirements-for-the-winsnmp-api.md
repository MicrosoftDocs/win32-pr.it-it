---
title: Requisiti software per l'API WinSNMP
description: Un'applicazione WinSNMP deve accedere all'API WinSNMP tramite la libreria a collegamento dinamico WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cf78c4937996a44b2a82ebeb0b2963f9a4ffaada0288068b07cd3b60432c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886071"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Requisiti software per l'API WinSNMP

Un'applicazione WinSNMP deve accedere all'API WinSNMP tramite la libreria a collegamento dinamico WSNMP32.DLL.

I file seguenti sono necessari per supportare la funzionalità dell'API WinSNMP.



| Nome file     | Descrizione                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. Lib  | Libreria WinSNMP                                                                              |
| WSNMP32.DLL  | Fornisce l'interfaccia WinSNMP                                                                   |
| WINSNMP. H    | File di intestazione WinSNMP                                                                          |
| SNMPTRAP.EXE | Riceve trap SNMP e le inoltra a MGMTAPI.DLL, la libreria API di Microsoft SNMP Manager |
| SNMPAPI.DLL  | Fornisce utilità SNMP                                                                      |



 

 

 




