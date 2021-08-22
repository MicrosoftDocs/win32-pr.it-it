---
title: Elenco alfabetico di tutte le funzioni WCS
description: Di seguito è riportato un elenco alfabetico completo delle funzioni API WCS 1.0 fornite da Windows \ 160;98 e versioni successive e Windows \ 160;2000 e versioni successive.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows Sistema di colori (WCS), funzioni
- WCS (Windows Color System), funzioni
- gestione del colore delle immagini, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Informazioni di riferimento su WCS, funzioni
- informazioni di riferimento per WCS, funzioni
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e2c9250cc9fb1e9e418079ed3b9524b3add2535dd780eed65ae998bda80ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706661"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Elenco alfabetico di tutte le funzioni WCS

Di seguito è riportato un elenco alfabetico completo delle funzioni api WCS 1.0 fornite da Windows 98 e versioni successive e Windows 2000 e versioni successive.



| Funzione o struttura                                                                 | Descrizione                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) è una funzione di callback implementata che aggiorna i dati di configurazione WCS durante l'esecuzione della finestra di dialogo visualizzata dalla funzione [**SetupColorMatchingW.**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associa un profilo colori specificato a un dispositivo specificato.                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Controlla se i pixel in una bitmap specificata si trovano all'interno della [gamma di](g.md) output di una trasformazione specificata. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina se i colori di una matrice si trovano all'interno della [gamma di](g.md) output di una trasformazione specificata. |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Controlla se i colori sono nella gamma di un dispositivo.                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Chiude un handle di profilo aperto. |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina se i colori specificati si trovano all'interno [della gamma di](./g.md) output di una trasformazione specificata. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina se le triple RGB specificate si trovano nella [gamma di](./g.md) output di una trasformazione specificata. |
| [**CMCheckRGB**](/windows/desktop/api/Wingdi/)                                                     | Controlla i colori delle bitmap rispetto a una gamma di output.                                                                                                        |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Converte i nomi dei colori in uno spazio colore denominato in numeri di indice in un profilo colori |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio colori denominato. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Crea un [profilo di collegamento del](./d.md) dispositivo nel formato specificato dall'International Color Consortium nella specifica ICC Profile Format Specification. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Accetta una matrice di profili o un singolo profilo [di collegamento del dispositivo](./d.md) e crea una trasformazione colore. Questa trasformazione è un mapping dallo spazio colore specificato dal primo profilo a quello del secondo profilo e così via all'ultimo. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Crea un profilo colori di visualizzazione da una [**struttura LOGCOLORSPACEA.**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Crea un profilo colori di visualizzazione da una [**struttura LOGCOLORSPACEW.**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Deprecato. Non esiste un'API sostitutiva perché questa non è più in uso. Gli sviluppatori di moduli CMM alternativi non sono necessari per implementarlo. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Crea una trasformazione di colore che esegue il mapping da un [**logCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) di input a uno spazio di destinazione facoltativo e quindi a un dispositivo di output, usando un set di flag che definiscono la modalità di creazione della trasformazione. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Crea una trasformazione di colore che esegue il mapping da un [**logCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) di input a uno spazio di destinazione facoltativo e quindi a un dispositivo di output, usando un set di flag che definiscono la modalità di creazione della trasformazione. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Deprecato. Non esiste un'API sostitutiva perché questa non è più in uso. Gli sviluppatori di moduli CMM alternativi non sono necessari per implementarlo. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Elimina una trasformazione di colore specificata e libera la memoria associata. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Recupera varie informazioni sul modulo di gestione del colore (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Recupera informazioni sul profilo colori denominato specificato. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | Ottiene un PostScript di rendering dei colori.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Recupera la finalità PostScript [rendering](rendering-intents.md) dei colori di livello 2 da un profilo. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | Ottiene una matrice PostScript spazio colore.                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Indica se il profilo specificato è un profilo ICC valido che può essere usato per la gestione del colore. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Converte una matrice di colori da uno spazio [colore di origine](color-spaces.md) a uno spazio colori di destinazione usando una trasformazione di colore. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Converte un RGBQuad fornito dall'applicazione nello spazio dei [colori del dispositivo.](color-spaces.md) |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Converte una bitmap da uno [spazio colore](color-spaces.md) a un altro usando una trasformazione di colore. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Converte una bitmap da un formato definito in un formato definito diverso e chiama periodicamente una funzione di callback, se specificata, per segnalare lo stato di avanzamento e consentire all'applicazione chiamante di terminare la conversione. |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Corregge le voci in un riquadro per un contesto di dispositivo.                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Esegue il mapping dei colori a scopo di anteprima.                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Converte i nomi dei colori in uno spazio colore denominato in numeri di indice in un profilo colori ICC (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio colori denominato. |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Crea uno spazio colore.                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio colori denominato. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Trasforma gli indici in uno spazio colore in una matrice di nomi in uno spazio colori denominato. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Accetta una matrice di profili o un singolo profilo di collegamento [del](d.md) dispositivo e crea una trasformazione colore che le applicazioni possono usare per eseguire il mapping dei colori. |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Converte uno spazio [colore logico in](c.md) un profilo di [dispositivo.](d.md) |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Elimina uno spazio colore.                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una trasformazione di colore specificata. |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Dissocia un profilo colori specificato con un dispositivo specificato in un computer specificato. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera tutti i profili che soddisfano i criteri di enumerazione specificati. |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Enumera i profili colori di output disponibili per un determinato contesto di dispositivo.                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | Funzione di callback definita dall'applicazione [**per EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera varie informazioni sul modulo di gestione colori (CMM) che ha creato la trasformazione del colore specificata. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera il percorso della directory Windows COLOR in un computer specificato. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia i dati da un elemento del profilo con tag specificato di un profilo colori specificato in un buffer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera il nome del tag specificato da *dwIndex* nella tabella dei tag di un profilo colori ICC (International Color Consortium) specificato, dove *dwIndex* è un indice in base uno in tale tabella. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Recupera il contenuto del profilo colori dato un handle per un profilo colori aperto.                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la struttura dell'intestazione ICC dal profilo colori ICC o dal profilo XML WCS. I driver e le applicazioni devono presupporre che la restituzione **di TRUE** indichi solo che viene restituita un'intestazione strutturata correttamente. Ogni tag dovrà comunque essere convalidato in modo indipendente usando le API ICM2 legacy o LE API di XML Schema. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ottiene lo spazio colore di input corrente in un contesto di dispositivo. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera il numero di elementi contrassegnati in un profilo colori specificato. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ottiene la rampa gamma dalle schede di visualizzazione a colori diretta.                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Ottiene il profilo colori di output corrente di un contesto di dispositivo.                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Ottiene la [**struttura LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) di un contesto di dispositivo.                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera informazioni sul profilo colori denominato ICC (International Color Consortium) specificato nel primo parametro. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera il dizionario PostScript rendering dei colori di livello 2 dal profilo colori ICC specificato. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera la finalità PostScript [rendering](r.md) dei colori di livello 2 da un profilo colori ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matrice PostScript spazio [colori](c.md) di livello 2 da un profilo colori ICC. |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera il profilo colori registrato per lo spazio colori standard [specificato.](c.md) |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | Callback fornito dall'applicazione per segnalare lo stato di avanzamento.                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installa un profilo specificato per l'uso in un computer specificato. Il profilo viene copiato anche nella directory COLOR. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica se un tag ICC (International Color Consortium) specificato è presente nel profilo colori specificato. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Consente di determinare se il profilo specificato è un profilo ICC (International Color Consortium) valido o un handle di profilo WCS (Windows Color System) valido che può essere usato per la gestione del colore. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un handle per un profilo colori specificato. L'handle può quindi essere usato in altre funzioni di gestione dei profili. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associa un valore di identificazione specificato alla libreria a collegamento dinamico (DLL CMM) del modulo di gestione colori specificata. Quando questo ID viene visualizzato in un profilo colori, Windows possibile individuare il CMM corrispondente in modo da creare una trasformazione. |
| [**Selezionare CMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Consente di selezionare il modulo CMM (Color Management Module) preferito da usare. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Imposta i dati dell'elemento per un elemento del profilo con tag in un profilo colori ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea in un profilo colori ICC specificato un nuovo tag che fa riferimento agli stessi dati di un tag esistente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Imposta le dimensioni di un elemento con tag in un profilo colori ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Imposta i dati dell'intestazione in un profilo colori ICC specificato. |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Imposta lo spazio colore di input di un contesto di dispositivo.                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Imposta la rampa gamma sulle schede di visualizzazione a colori diretto.                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Attiva o disattiva la gestione dei colori in un contesto di dispositivo.                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Imposta il profilo colori di output per un contesto di dispositivo specificato.                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un profilo specificato per uno spazio colore standard [specificato.](c.md) È possibile eseguire query sul profilo usando [GetStandardColorSpaceProfileW.](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Fornisce il controllo utente sulla gestione del colore tramite una finestra di dialogo.                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Converte i colori bitmap usando una trasformazione di colore.                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Converte una matrice di colori dallo spazio [colori di origine](c.md) allo spazio colori di destinazione come definito da una trasformazione di colore. |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Rimuove un profilo colori specificato da un computer specificato. I file associati vengono eliminati facoltativamente dal sistema. |
| [**Annullare la registrazione diCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Dissocia un valore ID specificato da una determinata libreria a collegamento dinamico del modulo di gestione colori (DLL CMM). |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associa un profilo colori WCS specificato a un dispositivo specificato.                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Determina se i colori in una matrice si trovano all'interno della gamma di output di una trasformazione di colori WCS specificata.                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Converte un profilo WCS in un profilo ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Dissocia un profilo colori WCS specificato con un dispositivo specificato in un computer specificato.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione dei profili specificato.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Restituisce le dimensioni, in byte, del buffer richiesto dalla funzione [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) per enumerare i profili colore. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina se la gestione del sistema dello stato di calibrazione dello schermo è abilitata.                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Recupera il profilo colori predefinito per un dispositivo o l'impostazione predefinita indipendente dal dispositivo se il dispositivo non è specificato.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Restituisce le dimensioni, in byte, del nome del profilo colori predefinito per un dispositivo, incluso il carattere **di terminazione NULL.**                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Restituisce la finalità di rendering dell'utente o del sistema.                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina se l'utente ha scelto di usare un elenco di associazioni del profilo per utente per il dispositivo specificato.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un handle per un profilo colori specificato.                                                                                                       |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Abilita o disabilita la gestione del sistema dello stato di calibrazione dello schermo.                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Imposta il nome del profilo colori predefinito del tipo di profilo specificato nell'ambito di gestione dei profili specificato.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Imposta la finalità di rendering a livello di utente o di sistema.                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Consente all'utente di specificare se usare o meno un elenco di associazioni del profilo per utente per il dispositivo specificato.                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Converte una matrice di colori dallo spazio colori di origine allo spazio colore di destinazione come definito da una trasformazione colore.                            |



 

 

 