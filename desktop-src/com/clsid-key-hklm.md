---
title: Chiave CLSID
description: Un CLSID è un identificatore univoco globale che identifica un oggetto classe COM. Se il server o il contenitore consente il collegamento ai relativi oggetti incorporati, è necessario registrare un CLSID per ogni classe supportata di oggetti.
ms.assetid: b5777d87-abf2-45b9-9d95-61db878a5810
keywords:
- Chiave del registro di sistema CLSID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9253446a039e47996366c7dfdb51c01f9b1993
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396442"
---
# <a name="clsid-key"></a>Chiave CLSID

Un CLSID è un identificatore univoco globale che identifica un oggetto classe COM. Se il server o il contenitore consente il collegamento ai relativi oggetti incorporati, è necessario registrare un CLSID per ogni classe supportata di oggetti.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ \_Classi software del computer locale \\ \\ \\ CLSID** \\ *{* CLSID *}*



| Chiave del Registro di sistema                                                 | Descrizione                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid.md)                                       | Associa un AppID a un CLSID.                                                                                                        |
| [**AutoConvertTo**](autoconvertto.md)                       | Specifica la conversione automatica di una determinata classe di oggetti in una nuova classe di oggetti.                                                |
| [**Autotreats**](autotreatas.md)                           | Imposta automaticamente il CLSID per la chiave [**Treats**](treatas.md) sul valore specificato.                                              |
| [**AuxUserType**](auxusertype.md)                           | Specifica il nome visualizzato breve e i nomi delle applicazioni di un'applicazione.                                                                     |
| [**Control**](control.md)                                   | Identifica un oggetto come controllo ActiveX.                                                                                              |
| [**Conversione**](conversion.md)                             | Utilizzato dalla finestra di dialogo **Converti** per determinare i formati che possono essere letti e scritti da un'applicazione.                                           |
| [**DataFormats**](dataformats.md)                           | Specifica i formati di dati predefiniti e principali supportati da un'applicazione.                                                                 |
| [**DefaultIcon**](defaulticon.md)                           | Fornisce informazioni sulle icone predefinite per le presentazioni iconiche degli oggetti.                                                                   |
| [**InprocHandler**](inprochandler.md)                       | Specifica se un'applicazione utilizza un gestore personalizzato.                                                                                  |
| [**InprocHandler32**](inprochandler32.md)                   | Specifica se un'applicazione utilizza un gestore personalizzato.                                                                                  |
| [**InprocServer**](inprocserver.md)                         | Specifica il percorso della DLL del server in-process.                                                                                         |
| [**InprocServer32**](inprocserver32.md)                     | Registra un server in-process a 32 bit e specifica il modello di threading dell'Apartment in cui è possibile eseguire il server.                           |
| [**Inseribile**](insertable.md)                             | Indica che gli oggetti di questa classe devono essere visualizzati nella casella di riepilogo della finestra di dialogo **Inserisci oggetto** quando vengono utilizzati dalle applicazioni contenitore com. |
| [**Interfaccia**](interface.md)                               | Voce facoltativa che specifica tutti gli ID di interfaccia (IID) supportati dalla classe associata.                                             |
| [**LocalServer**](localserver.md)                           | Specifica il percorso completo di un'applicazione server locale a 16 bit.                                                                            |
| [**LocalServer32**](localserver32.md)                       | Specifica il percorso completo di un'applicazione server locale a 32 bit.                                                                            |
| [**MiscStatus**](miscstatus.md)                             | Specifica la modalità di creazione e visualizzazione di un oggetto.                                                                                           |
| [**ProgID**](progid.md)                                     | Associa un ProgID a un CLSID.                                                                                                        |
| [**ToolBoxBitmap32**](toolboxbitmap32.md)                   | Identifica il nome del modulo e l'ID di risorsa per una bitmap 16 x 16 da usare per la superficie di una barra degli strumenti o un pulsante della casella degli strumenti.                      |
| [**TreatAs**](treatas.md)                                   | Specifica il CLSID di una classe in grado di emulare la classe corrente.                                                                       |
| [**Verbo**](verb.md)                                         | Specifica i verbi da registrare per un'applicazione.                                                                                 |
| [**Versione**](version.md)                                   | Specifica il numero di versione del controllo.                                                                                             |
| [**VersionIndependentProgID**](versionindependentprogid.md) | Associa un ProgID a un CLSID. Questo valore viene utilizzato per determinare la versione più recente di un'applicazione dell'oggetto.                           |



 

## <a name="remarks"></a>Commenti

La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.

La chiave CLSID contiene le informazioni utilizzate dal gestore COM predefinito per restituire informazioni su una classe quando si trova nello stato in esecuzione.

Per ottenere un CLSID per l'applicazione, è possibile utilizzare il Uuidgen.exe oppure utilizzare la funzione [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .

Il CLSID è un numero a 128 bit, in formato esadecimale, all'interno di una coppia di parentesi graffe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid)
</dt> </dl>

 

 




