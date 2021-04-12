---
description: Le bitmap dipendenti dal dispositivo (DDB) vengono descritte usando una singola struttura, la struttura BITMAP.
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Bitmap Device-Dependent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a3de2c59509c71b38f9981df330b3b28effa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130798"
---
# <a name="device-dependent-bitmaps"></a>Bitmap Device-Dependent

Le bitmap dipendenti dal dispositivo (DDB) vengono descritte usando una singola struttura, la struttura [**bitmap**](/windows/win32/api/wingdi/ns-wingdi-bitmap) . I membri di questa struttura specificano la larghezza e l'altezza di un'area rettangolare, in pixel; larghezza della matrice che esegue il mapping delle voci dalla tavolozza del dispositivo ai pixel; e il formato colori del dispositivo, in termini di piani di colore e bit per pixel. Un'applicazione può recuperare il formato di colore di un dispositivo chiamando la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e specificando le costanti appropriate. Si noti che un DDB non contiene valori di colore; i colori sono invece in un formato dipendente dal dispositivo. Per altre informazioni, vedere [color in bitmaps](color-in-bitmaps.md). Poiché ogni dispositivo può avere un proprio set di colori, un DDB creato per un dispositivo potrebbe non essere visualizzato correttamente in un dispositivo diverso.

Per usare un DDB in un contesto di dispositivo, deve avere l'organizzazione dei colori del contesto del dispositivo. In questo modo, un DDB viene spesso definito *bitmap compatibile* e in genere offre prestazioni GDI migliori rispetto a una DIB. Ad esempio, per creare una bitmap per la memoria video, è preferibile usare una bitmap compatibile con lo stesso formato di colore dello schermo principale. Una volta nella memoria video, il rendering nella bitmap e la relativa visualizzazione sullo schermo sono molto più veloci rispetto a una superficie di memoria di sistema o direttamente da una DIB.

Oltre ad abilitare prestazioni GDI migliori, le bitmap compatibili vengono usate per acquisire immagini (vedere [acquisizione di un'immagine](capturing-an-image.md) ) e per creare bitmap in fase di esecuzione per i menu vedere "creazione della bitmap" in (vedere [using menus](../menurc/using-menus.md) ).

Per trasferire una bitmap tra dispositivi con diverse organizzazioni di colori, usare [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) per convertire la bitmap compatibile in una DIB e chiamare [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) per visualizzare la DIB nel secondo dispositivo.

Esistono due tipi di DDB: uncardable e non eliminabile. Un DDB scartabile è una bitmap che il sistema rimuove se la bitmap non è selezionata in un controller di dominio e se la memoria di sistema è insufficiente. La funzione [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) crea bitmap ignorabili. Le funzioni [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)e [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) creano bitmap non eliminabili.

Un'applicazione può creare un DDB da una DIB inizializzando le strutture necessarie e chiamando la funzione [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) . Specificare CBM \_ init nella chiamata a **CreateDIBitmap** equivale a chiamare la funzione [**CREATECOMPATIBLEBITMAP**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) per creare un DDB nel formato del dispositivo e quindi chiamare la funzione [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) per convertire i bit DIB in DDB. Per determinare se un dispositivo supporta la funzione **SetDIBits** , chiamare la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) specificando la \_ bitmap RC di \_ come flag RasterCaps.

 

 
