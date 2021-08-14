---
description: Negli esempi seguenti viene utilizzata la funzione SetStringInBlob per creare voci BLOB speciali.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Voci BLOB speciali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0659fa05219dcc715c6c00b3d28635e2500f73e4e5bece72049ee43839a0820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363139"
---
# <a name="special-blob-entries"></a>Voci BLOB speciali

Negli esempi seguenti viene utilizzata [**la funzione SetStringInBlob**](setstringinblob.md) per creare voci BLOB speciali.

## <a name="npp-name"></a>Nome NPP

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a>Identificatore di classe NPP

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a>Nome procedura CFGPROC

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a>Nome radice albero per l'interfaccia utente di Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a>Stringa di visualizzazione per l'interfaccia utente di Finder

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a>Tag di interfaccia

Questo esempio include tutte le interfacce supportate da NPP.

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



