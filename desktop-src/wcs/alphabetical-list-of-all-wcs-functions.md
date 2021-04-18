---
title: Elenco alfabetico di tutte le funzioni WCS
description: Di seguito è riportato un elenco alfabetico completo delle funzioni dell'API WCS 1,0 fornite da Windows \ 160; 98 e versioni successive e Windows \ 160; 2000 e versioni successive.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b70208c1f1f7d87b4f5cd6f4a14f3f22e0bc2f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320945"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Elenco alfabetico di tutte le funzioni WCS

Di seguito è riportato un elenco alfabetico completo delle funzioni dell'API WCS 1,0 fornite da Windows 98 e versioni successive e Windows 2000 e versioni successive.



| Funzione o struttura                                                                 | Descrizione                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) è una funzione di callback implementata che aggiorna i dati di configurazione di WCS mentre è in esecuzione la finestra di dialogo visualizzata dalla funzione [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) . |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associa un profilo colori specificato a un dispositivo specificato.                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Verifica se i pixel in una bitmap specificata si trovano all'interno del [gamut](g.md) di output di una trasformazione specificata. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina se i colori in una matrice si trovano all'interno del [gamut](g.md) di output di una trasformazione specificata. |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Controlla se i colori specificati si trovano nel gamut del dispositivo.                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Chiude un handle del profilo aperto. |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina se i colori specificati si trovano all'interno del [gamut](./g.md) di output di una trasformazione specificata. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina se i tripli RGB specificati si trovano nel [gamut](./g.md) di output di una trasformazione specificata. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                                     | Verifica i colori bitmap rispetto a un gamut di output.                                                                                                        |
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
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | Ottiene un dizionario di rendering del colore PostScript.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Recupera lo [scopo del rendering](rendering-intents.md) dei colori a livello 2 del post-script da un profilo. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | Ottiene una matrice dello spazio del colore del post-script.                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Segnala se il profilo specificato è un profilo ICC valido che può essere utilizzato per la gestione dei colori. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Converte una matrice di colori da uno [spazio colore](color-spaces.md) di origine a uno spazio colore di destinazione usando una trasformazione colore. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Converte una RGBQuad fornita dall'applicazione nello [spazio dei colori](color-spaces.md)del dispositivo. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Converte una bitmap da uno [spazio colore](color-spaces.md) a un altro utilizzando una trasformazione colore. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Converte una bitmap da un formato definito in un formato definito diverso e chiama una funzione di callback periodicamente, se ne viene specificata una, per segnalare lo stato di avanzamento e consentire all'applicazione chiamante di terminare la traduzione. |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Corregge le voci in una tavolozza per un contesto di dispositivo.                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Esegue il mapping dei colori a scopo di anteprima.                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Converte i nomi di colore in uno spazio di colore denominato per indicizzare i numeri in un profilo colori ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio dei colori denominato. |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Crea uno spazio colore.                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio dei colori denominato. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio dei colori denominato. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Accetta una matrice di profili o un singolo [profilo di collegamento del dispositivo](d.md) e crea una trasformazione colore che le applicazioni possono usare per eseguire il mapping dei colori. |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Converte uno [spazio di colore](c.md) logico in un [profilo di dispositivo](d.md). |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Elimina uno spazio colore.                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una trasformazione colore specificata. |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Annulla l'associazione di un profilo colori specificato a un dispositivo specificato in un computer specificato. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera tutti i profili che soddisfano i criteri di enumerazione specificati. |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Enumera i profili dei colori di output disponibili per un determinato contesto di dispositivo.                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | Funzione di callback definita dall'applicazione per [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera varie informazioni sul modulo di gestione colori (CMM) che ha creato la trasformazione colore specificata. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera il percorso della directory dei colori di Windows in un computer specificato. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia i dati da un elemento profilo con tag specificato di un profilo colori specificato in un buffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera il nome del tag specificato da *dwIndex* nella tabella dei tag di un profilo colori ICC (International Color Consortium) specificato, in cui *dwIndex* è un indice in base uno in tale tabella. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Recupera il contenuto del profilo colori dato un handle a un profilo colori aperto.                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la struttura di intestazione ICC da profilo colori ICC o dal profilo XML WCS. I driver e le applicazioni devono presupporre che restituisca **true** solo indica che viene restituita un'intestazione strutturata correttamente. Ogni tag dovrà comunque essere convalidato in modo indipendente usando API ICM2 legacy o API XML Schema. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ottiene lo spazio del colore di input corrente in un contesto di dispositivo. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera il numero di elementi contrassegnati in un profilo colori specificato. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ottiene la rampa gamma dalle lavagne di visualizzazione a colori diretti.                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Ottiene il profilo del colore di output corrente di un contesto di dispositivo.                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Ottiene la struttura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) di un contesto di dispositivo.                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera le informazioni sul profilo colori International Color Consortium (ICC) indicato nel primo parametro. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera il dizionario per il rendering del colore di livello 2 PostScript dal profilo colori ICC specificato. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera lo [scopo del rendering](r.md) dei colori a livello 2 del post-script da un profilo colori ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matrice di spazi dei [colori](c.md) di livello 2 PostScript da un profilo colori ICC. |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera il profilo colori registrato per lo spazio dei [colori](c.md)standard specificato. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | Callback fornito dall'applicazione per segnalare lo stato di avanzamento.                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installa un determinato profilo da usare in un computer specificato. Il profilo viene anche copiato nella directory dei colori. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica se nel profilo colori specificato è presente un tag ICC (International Color Consortium) specificato. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Consente di determinare se il profilo specificato è un profilo ICC (International Color Consortium) valido o un handle del profilo WCS (Windows Color System) valido che può essere utilizzato per la gestione dei colori. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un handle per un profilo colori specificato. L'handle può quindi essere utilizzato in altre funzioni di gestione dei profili. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associa un valore di identificazione specificato al modulo di gestione dei colori specificato (libreria a collegamento dinamico). Quando questo ID viene visualizzato in un profilo colori, Windows può individuare il CMM corrispondente in modo da creare una trasformazione. |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Consente di selezionare il modulo di gestione colori (CMM) preferito da usare. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Imposta i dati dell'elemento per un elemento del profilo con tag in un profilo colori ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea in un profilo colori ICC specificato un nuovo tag che fa riferimento agli stessi dati di un tag esistente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Imposta la dimensione di un elemento con tag in un profilo colori ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Imposta i dati dell'intestazione in un profilo colori ICC specificato. |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Imposta lo spazio colore di input di un contesto di dispositivo.                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Imposta la rampa gamma sulle lavagne di visualizzazione a colori diretti.                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Attiva o disattiva la gestione dei colori in un contesto di dispositivo.                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Imposta il profilo del colore di output per un contesto di dispositivo specificato.                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un profilo specificato per un determinato [spazio dei colori](c.md)standard. È possibile eseguire query sul profilo utilizzando [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Fornisce il controllo utente sulla gestione dei colori tramite una finestra di dialogo.                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Converte i colori bitmap utilizzando una trasformazione colore.                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Converte una matrice di colori dallo [spazio del colore](c.md) di origine allo spazio dei colori di destinazione in base a quanto definito da una trasformazione colore. |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Rimuove un profilo colori specificato da un computer specificato. Facoltativamente, i file associati vengono eliminati dal sistema. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Annulla l'associazione di un valore ID specificato da una libreria di collegamento dinamico (DLL) del modulo di gestione colori specificata. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associa un profilo colori WCS specificato a un dispositivo specificato.                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Determina se i colori in una matrice si trovano all'interno del gamut di output di una trasformazione del colore WCS specificata.                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Converte un profilo WCS in un profilo ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Annulla l'associazione di un profilo colori WCS specificato a un dispositivo specifico in un computer specificato.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione del profilo specificato.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Restituisce la dimensione, in byte, del buffer richiesto dalla funzione [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) per enumerare i profili colori. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina se è abilitata la gestione del sistema dello stato di calibrazione dello schermo.                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Recupera il profilo colori predefinito per un dispositivo o l'impostazione predefinita indipendente dal dispositivo se il dispositivo non è specificato.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Restituisce la dimensione, in byte, del nome del profilo colori predefinito per un dispositivo, incluso il carattere di terminazione **null** .                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Restituisce l'utente o la finalità di rendering a livello di sistema.                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina se l'utente ha scelto di usare un elenco di associazioni del profilo per utente per il dispositivo specificato.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un handle per un profilo colori specificato.                                                                                                       |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Abilita o Disabilita la gestione del sistema dello stato di calibrazione dello schermo.                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Imposta il nome del profilo colori predefinito del tipo di profilo specificato nell'ambito di gestione del profilo specificato.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Imposta l'intento di rendering a livello di utente o di sistema.                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Consente all'utente di specificare se utilizzare o meno un elenco di associazioni del profilo per utente per il dispositivo specificato.                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Converte una matrice di colori dallo spazio del colore di origine allo spazio dei colori di destinazione in base a quanto definito da una trasformazione colore.                            |



 

 

 