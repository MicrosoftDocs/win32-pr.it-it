---
title: Requisiti software per l'API WinSNMP
description: Un'applicazione WinSNMP deve accedere all'API WinSNMP tramite la libreria a collegamento dinamico WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220903"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Requisiti software per l'API WinSNMP

Un'applicazione WinSNMP deve accedere all'API WinSNMP tramite la libreria a collegamento dinamico WSNMP32.DLL.

I file seguenti sono necessari per supportare la funzionalità dell'API WinSNMP.



| Nome file     | Descrizione                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| Wsnmp32. LIB  | Libreria WinSNMP                                                                              |
| WSNMP32.DLL  | Fornisce l'interfaccia WinSNMP                                                                   |
| WINSNMP. H    | File di intestazione WinSNMP                                                                          |
| SNMPTRAP.EXE | Riceve trap SNMP e li inoltra al MGMTAPI.DLL, la libreria API Microsoft SNMP Manager |
| SNMPAPI.DLL  | Fornisce utilità SNMP                                                                      |



 

 

 




