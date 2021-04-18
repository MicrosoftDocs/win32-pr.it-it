---
title: Funzioni WCS per i moduli di gestione colori (CMM) da implementare
description: Le funzioni seguenti devono essere implementate da moduli di gestione colori (CMM) ed esportate per il sistema operativo da chiamare.
ms.assetid: e05129ec-9128-44f0-82c7-f4e01536d7a8
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
- Windows Color System (WCS), modulo di gestione colori (CMM)
- WCS (sistema di colori Windows), modulo Gestione colori (CMM)
- Gestione colori immagine, modulo di gestione colori (CMM)
- gestione dei colori, modulo di gestione colori (CMM)
- colori, modulo di gestione colori (CMM)
- Guida di riferimento a WCS, modulo Gestione colori
- informazioni di riferimento per WCS, modulo di gestione colori (CMM)
- Modulo di gestione colori (CMM)
- CMM (modulo di gestione colori)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e9092c49077b1b4dda9e06829329194ec2e261
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320877"
---
# <a name="wcs-functions-for-color-management-modules-cmms-to-implement"></a>Funzioni WCS per i moduli di gestione colori (CMM) da implementare

Le funzioni seguenti devono essere implementate da moduli di gestione colori (CMM) ed esportate per il sistema operativo da chiamare.



| Funzione                                                                     | Descrizione                                                                               |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina se i colori specificati si trovano all'interno del [gamut](./g.md) di output di una trasformazione specificata. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina se i tripli RGB specificati si trovano nel [gamut](./g.md) di output di una trasformazione specificata. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                           | Verifica i colori bitmap rispetto a un gamut di output.                                             |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Converte i nomi di colore in uno spazio di colore denominato per indicizzare i numeri in un profilo colori |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio dei colori denominato. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Crea un [profilo di collegamento al dispositivo](./d.md) nel formato specificato da International Color Consortium nella specifica del formato del profilo ICC. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Accetta una matrice di profili o un [profilo di collegamento a dispositivo](./d.md) singolo e crea una trasformazione colore. Questa trasformazione è un mapping dallo spazio dei colori specificato dal primo profilo a quello del secondo profilo e così via all'ultima. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Crea un profilo colori di visualizzazione da una struttura [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) . |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Crea un profilo colori di visualizzazione da una struttura [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) . |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Deprecato. Non è presente alcuna API sostitutiva perché non è più usata. Gli sviluppatori di moduli CMM alternativi non devono implementarla. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Crea una trasformazione colore che esegue il mapping da un [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) di input a uno spazio di destinazione facoltativo e quindi a un dispositivo di output, usando un set di flag che definiscono la modalità di creazione della trasformazione. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Crea una trasformazione colore che esegue il mapping da un [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) di input a uno spazio di destinazione facoltativo e quindi a un dispositivo di output, usando un set di flag che definiscono la modalità di creazione della trasformazione. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Deprecato. Non è presente alcuna API sostitutiva perché non è più usata. Gli sviluppatori di moduli CMM alternativi non devono implementarla. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Elimina una trasformazione colore specificata e libera la memoria associata. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Recupera varie informazioni sul modulo di gestione colori (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Recupera le informazioni sul profilo colori denominato specificato. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/) | Ottiene un dizionario di rendering del colore PostScript.                                             |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Recupera lo [scopo del rendering](rendering-intents.md) dei colori a livello 2 del post-script da un profilo. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                   | Ottiene una matrice dello spazio del colore del post-script.                                                      |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Segnala se il profilo specificato è un profilo ICC valido che può essere utilizzato per la gestione dei colori. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Converte una matrice di colori da uno [spazio colore](rendering-intents.md) di origine a uno spazio colore di destinazione usando una trasformazione colore. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Converte una RGBQuad fornita dall'applicazione nello [spazio dei colori](color-spaces.md)del dispositivo. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Converte una bitmap da uno [spazio colore](color-spaces.md) a un altro utilizzando una trasformazione colore. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Converte una bitmap da un formato definito in un formato definito diverso e chiama una funzione di callback periodicamente, se ne viene specificata una, per segnalare lo stato di avanzamento e consentire all'applicazione chiamante di terminare la traduzione. |



 

 

 