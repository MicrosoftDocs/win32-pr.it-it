---
title: Chiave CLSID
description: Un CLSID è un identificatore univoco globale che identifica un oggetto classe COM. Se il server o il contenitore consente il collegamento ai relativi oggetti incorporati, è necessario registrare un CLSID per ogni classe di oggetti supportata.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- CHIAVE DEL Registro DI SISTEMA CLSID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd390fc6a1ccb15e128245c3b6a80e2b4ca57f41de9e9c21e93ebe4c708783d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854981"
---
# <a name="clsid-key"></a>Chiave CLSID

Un CLSID è un identificatore univoco globale che identifica un oggetto classe COM. Se il server o il contenitore consente il collegamento ai relativi oggetti incorporati, è necessario registrare un CLSID per ogni classe di oggetti supportata.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ \_ \\ CLSID classi SOFTWARE \\ \\ LOCAL MACHINE** \\ *{* CLSID *}*



| Chiave del Registro di sistema                                                 | Descrizione                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Appid**](appid.md)                                       | Associa un AppID a un CLSID.                                                                                                        |
| [**AutoConvertTo**](autoconvertto.md)                       | Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti.                                                |
| [**AutoTreatAs**](autotreatas.md)                           | Imposta automaticamente il CLSID per [**la chiave TreatAs**](treatas.md) sul valore specificato.                                              |
| [**AuxUserType**](auxusertype.md)                           | Specifica il nome visualizzato breve di un'applicazione e i nomi delle applicazioni.                                                                     |
| [**Control**](control.md)                                   | Identifica un oggetto come controllo ActiveX controllo .                                                                                              |
| [**Conversione**](conversion.md)                             | Utilizzato dalla finestra **di dialogo** Converti per determinare i formati che un'applicazione può leggere e scrivere.                                           |
| [**Dataformats**](dataformats.md)                           | Specifica i formati di dati predefiniti e principali supportati da un'applicazione.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Fornisce informazioni sulle icone predefinite per presentazioni di oggetti icona.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Specifica se un'applicazione usa un gestore personalizzato.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Specifica se un'applicazione usa un gestore personalizzato.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Specifica il percorso della DLL del server in-process.                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | Registra un server in-process a 32 bit e specifica il modello di threading dell'apartment in cui può essere eseguito il server.                           |
| [**Inseribile**](insertable.md)                             | Indica che gli oggetti di questa classe devono essere visualizzati nella casella **di** riepilogo Della finestra di dialogo Inserisci oggetto quando vengono usati dalle applicazioni contenitore COM. |
| [**Interfaccia**](interface.md)                               | Voce facoltativa che specifica tutti gli ID di interfaccia (IID) supportati dalla classe associata.                                             |
| [**LocalServer**](localserver.md)                           | Specifica il percorso completo di un'applicazione server locale a 16 bit.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Specifica il percorso completo di un'applicazione server locale a 32 bit.                                                                            |
| [**MiscStatus**](miscstatus.md)                             | Specifica come creare e visualizzare un oggetto .                                                                                           |
| [**ProgID**](progid.md)                                     | Associa un ProgID a un CLSID.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifica il nome del modulo e l'ID risorsa per una bitmap 16 x 16 da usare per il viso di una barra degli strumenti o di un pulsante della casella degli strumenti.                      |
| [**TreatAs**](treatas.md)                                   | Specifica il CLSID di una classe che può emulare la classe corrente.                                                                       |
| [**Verbo**](verb.md)                                         | Specifica i verbi da registrare per un'applicazione.                                                                                 |
| [**Versione**](version.md)                                   | Specifica il numero di versione del controllo.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Associa un ProgID a un CLSID. Questo valore viene usato per determinare la versione più recente di un'applicazione oggetto.                           |



 

## <a name="remarks"></a>Commenti

La **chiave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corrisponde alla chiave **HKEY CLASSES \_ \_ ROOT,** che è stata mantenuta per garantire la compatibilità con le versioni precedenti di COM.

La chiave CLSID contiene informazioni usate dal gestore COM predefinito per restituire informazioni su una classe quando è in esecuzione.

Per ottenere un CLSID per l'applicazione, è possibile usare il Uuidgen.exe o la [**funzione CoCreateGuid.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)

IL CLSID è un numero a 128 bit, in formato esadecimale, all'interno di una coppia di parentesi graffe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Cocreateguid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




