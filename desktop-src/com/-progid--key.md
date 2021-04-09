---
title: Chiave ProgID
description: Un identificatore a livello di codice (ProgID) è una voce del registro di sistema che può essere associata a un CLSID. Analogamente al CLSID, ProgID identifica una classe ma con minore precisione perché non è garantita l'univocità globale.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047730"
---
# <a name="progid-key"></a>Chiave ProgID

Un identificatore a livello di codice (ProgID) è una voce del registro di sistema che può essere associata a un CLSID. Analogamente al CLSID, ProgID identifica una classe ma con minore precisione perché non è garantita l'univocità globale.

## <a name="registry-entry"></a>Voce del Registro di sistema

**HKEY \_ \_ \\ \\ Classi software del computer locale** \\ *{* ProgID *}*



| Chiave del Registro di sistema                            | Descrizione                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [**CLSID**](clsid.md)                  | Associa un ProgID a un CLSID.                                  |
| [**Inseribile**](insertable-progid.md) | Indica che questa classe è inseribile nei contenitori OLE 2.       |
| [**Protocollo**](protocol.md)            | Indica che questa classe OLE 2 è inseribile nei contenitori OLE 1. |
| [**Shell**](shell.md)                  | Fornisce informazioni sulla stampa della shell di Windows 3,1 e sui **file aperti** . |



 

## <a name="remarks"></a>Commenti

È possibile usare un ProgID in situazioni di programmazione in cui non è possibile usare un CLSID. I ProgID non devono essere visualizzati nell'interfaccia utente. Non è garantito che i ProgID siano univoci, quindi possono essere usati solo quando i conflitti di nomi sono gestibili.

Il formato di un ProgID è <*Program*>. <*Component*>. <*versione*>, separati da punti e senza spazi, come in Word.Document. 6. Il ProgID deve essere conforme ai requisiti seguenti:

-   Non sono presenti più di 39 caratteri.
-   Non contengono segni di punteggiatura (inclusi i caratteri di sottolineatura) tranne uno o più punti.
-   Non iniziare con una cifra.
-   Essere diverso dal nome della classe di qualsiasi applicazione OLE 1, inclusa la versione OLE 1 della stessa applicazione, se presente.

Poiché il ProgID non dovrebbe essere visualizzato nell'interfaccia utente, è possibile ottenere un nome visualizzabile chiamando [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype). Vedere anche [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).

La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




