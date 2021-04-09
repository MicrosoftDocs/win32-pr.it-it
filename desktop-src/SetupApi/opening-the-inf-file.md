---
description: È necessario utilizzare la funzione SetupOpenInfFile per aprire il file INF prima di poter recuperare informazioni da esso o aggiungere altri file INF.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Apertura del file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882362"
---
# <a name="opening-the-inf-file"></a>Apertura del file INF

È necessario utilizzare la funzione [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) per aprire il file inf prima di poter recuperare informazioni da esso o aggiungere altri file inf.

Il codice seguente apre un file INF con [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) e restituisce un handle, MyInf, al file inf aperto. Il parametro *InfClass* di **SetupOpenInfFile** è specificato come **null** per indicare che la classe del file inf deve essere ignorata.


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



Dopo l'apertura di un file INF, è possibile chiamare la funzione [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) per aggiungere un file al file inf aperto. Per aggiungere più file, ripetere questo processo. Se si chiama la funzione **SetupOpenAppendInfFile** e il nome file passato è **null**, la funzione cercherà nella sezione Version del file inf aperto (e di eventuali file inf aggiunti) una chiave LayoutFile. Se la funzione trova una chiave, verrà aggiunto il file specificato da tale chiave, in genere LAYOUT. INF). Quando più file INF sono stati combinati, **SetupOpenAppendInfFile** inizia con l'ultimo file inf accodato durante la ricerca di una sezione di versione.

 

 



