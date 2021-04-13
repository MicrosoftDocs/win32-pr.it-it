---
title: Chiave ProgID indipendente dalla versione
description: Associa un ProgID a un CLSID. Questa chiave viene utilizzata per determinare la versione più recente di un'applicazione per oggetti.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474909"
---
# <a name="version-independent-progid-key"></a>Chiave ProgID indipendente dalla versione

Associa un ProgID a un CLSID. Questa chiave viene utilizzata per determinare la versione più recente di un'applicazione per oggetti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Commenti

La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.

Il formato per <*ProgID indipendente dalla versione*> è <*program*>. <*componente*>, separato da punti, senza spazi e nessun numero di versione. Il ProgID indipendente dalla versione, come il ProgID, può essere registrato con un nome leggibile.

*ProgID* è il ProgID della versione installata più recente della classe.

Le applicazioni devono registrare un identificatore programmatico indipendente dalla versione sotto la chiave *ProgID indipendente dalla versione* . Il ProgID indipendente dalla versione si riferisce alla classe dell'applicazione e non passa da una versione all'altra, rimanendo invece costante in tutte le versionsâ € ", ad esempio, il documento di Microsoft Word. Viene usato con i linguaggi macro e si riferisce alla versione attualmente installata della classe dell'applicazione. Il ProgID indipendente dalla versione deve corrispondere al nome della versione più recente dell'applicazione dell'oggetto.

Ad esempio, il ProgID indipendente dalla versione viene utilizzato quando un'applicazione contenitore crea un grafico o una tabella con un pulsante della barra degli strumenti. In questa situazione, l'applicazione può utilizzare il ProgID indipendente dalla versione per determinare la versione più recente dell'applicazione oggetto necessaria.

Il ProgID indipendente dalla versione viene archiviato e gestito esclusivamente dal codice dell'applicazione. Quando viene specificato il ProgID indipendente dalla versione, la funzione [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) restituisce il CLSID della versione corrente.

È possibile usare [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) per eseguire la conversione tra queste due rappresentazioni.

È possibile usare [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) o [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) per modificare l'identificatore in una stringa visualizzabile.

Se non viene usato un gestore personalizzato, la voce deve essere impostata su OLE32.DLL, come illustrato nell'esempio seguente:

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<ProgID> Chiave](-progid--key.md)
</dt> </dl>

 

 




