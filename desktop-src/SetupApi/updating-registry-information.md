---
description: Al termine del commit della coda, sarà necessario aggiornare le informazioni del Registro di sistema per il prodotto che si sta installando.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Aggiornamento delle informazioni del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579ef64739bbe063d6fed19234a74b89b86b8b257793a1a26e83fd651256d189
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683051"
---
# <a name="updating-registry-information"></a>Aggiornamento delle informazioni del Registro di sistema

Al termine del commit della coda, sarà necessario aggiornare le informazioni del Registro di sistema per il prodotto che si sta installando. È consigliabile attendere il completamento di tutte le operazioni di copia file necessarie prima di modificare le informazioni del Registro di sistema.

Un modo per aggiornare il Registro di sistema è chiamare [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) con i flag SPINST \_ INIFILES, SPINST REGISTRY o \_ SPINST \_ INI2REG specificati. Questi flag possono essere combinati in una sola chiamata a **SetupInstallFromInfSection**.

L'esempio seguente usa SPINST ALL^SPINST FILES per indicare che la funzione deve elaborare tutte le operazioni \_ elencate, ad eccezione delle operazioni sui \_ file. Poiché nella sezione Install sono elencate solo  le operazioni INI, registry e file, si tratta di un metodo abbreviato per specificare che la funzione deve elaborare tutte le operazioni INI e del Registro di sistema.

L'esempio seguente illustra come installare le informazioni del Registro di sistema usando la **funzione SetupInstallFromINFSection.**

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

Nell'esempio *OwnerWindow* è **NULL** perché solo le operazioni sui file generano finestre di dialogo e pertanto non è necessaria una finestra padre. "MyInf" è il file INF contenente la sezione da elaborare. Il parametro "MySection" specifica la sezione da installare. I flag combinati, SPINST ALL ^ SPINST FILES, specificano le operazioni di installazione da elaborare, in questo caso tutte le operazioni \_ tranne le operazioni sui \_ file. Il percorso radice di origine viene specificato come "A: \\ ".

Poiché non viene elaborata alcuna operazione di copia, i parametri *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* e *DeviceInfoData* non sono specificati.

 

 



