---
title: LIBMAIN. CPP
description: Nel componente provider di esempio, un esempio di codice del punto di ingresso della DLL standard per Adssmp.dll è in LibMain. cpp. Le routine supportate sono elencate nella tabella seguente.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297668"
---
# <a name="libmaincpp"></a>LIBMAIN. CPP

Nel componente provider di esempio, un esempio di codice del punto di ingresso della DLL standard per Adssmp.dll è in LibMain. cpp. Le routine supportate sono elencate nella tabella seguente.



| Elemento                                  | Descrizione                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| **DllGetClassObject**<br/>      | Punto di ingresso della DLL standard per individuare le class factory.<br/>        |
| **DllCanUnloadNow**<br/>        | Punto di ingresso DLL standard per determinare se la DLL può essere scaricata.<br/> |
| **LibMain**<br/>                | Punto di ingresso di inizializzazione DLL standard.<br/>                      |
| **IsCompatibleOleVersion**<br/> | Verificare la compatibilità con la fase di esecuzione OLE.<br/>                   |
| **DllMain**<br/>                | Punto di ingresso per la maggior parte delle versioni di Windows 2000 o Windows NT.<br/>     |



 

 

 





