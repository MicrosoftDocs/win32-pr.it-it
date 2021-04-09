---
description: Una volta aperto il file INF, è possibile raccogliere informazioni da esso per compilare l'interfaccia utente o per indirizzare il processo di installazione. Le funzioni di installazione forniscono diversi livelli di funzionalità per la raccolta di informazioni da un file INF.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Estrazione di informazioni sui file dal file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879642"
---
# <a name="extracting-file-information-from-the-inf-file"></a>Estrazione di informazioni sui file dal file INF

Una volta aperto il file INF, è possibile raccogliere informazioni da esso per compilare l'interfaccia utente o per indirizzare il processo di installazione. Le funzioni di installazione forniscono diversi livelli di funzionalità per la raccolta di informazioni da un file INF.



| Per raccogliere informazioni...                | Usa queste funzioni...                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| Informazioni sul file INF                    | [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa). |
| Informazioni sui file di origine e di destinazione         | [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| Da una riga di un file INF            | [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| Da un campo di una riga in un file INF | [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

Nell'esempio seguente viene usata la funzione [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) per recuperare la descrizione leggibile di un supporto di origine da un file inf.


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



Nell'esempio, MyInf è l'handle per il file INF aperto. SourceId è l'identificatore per un supporto di origine specifico. Il valore SRCINFO \_ Description specifica che la funzione [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) deve recuperare la descrizione del supporto di origine. Il buffer punta a una stringa che riceverà la descrizione, MaxBufSize indica le risorse allocate al buffer e BufSize indica le risorse necessarie per archiviare il buffer.

Se BufSize è maggiore di MaxBufSize, la funzione restituirà **false** e una chiamata successiva a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà un errore \_ di \_ buffer insufficiente.

 

 
