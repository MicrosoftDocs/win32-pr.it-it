---
title: Chiave ProgID indipendente dalla versione
description: Associa un ProgID a un CLSID. Questa chiave viene usata per determinare la versione più recente di un'applicazione oggetto.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad09f9d86c2f34d93757e940c5262cd294485ad5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883144"
---
# <a name="version-independent-progid-key"></a>Chiave ProgID indipendente dalla versione

Associa un ProgID a un CLSID. Questa chiave viene usata per determinare la versione più recente di un'applicazione oggetto.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a>Commenti

La **chiave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corrisponde alla chiave **HKEY CLASSES \_ \_ ROOT,** che è stata mantenuta per la compatibilità con le versioni precedenti di COM.

Il formato per <*ProgID* indipendente dalla versione> è <programma *>.<* *component*>, separato da punti, nessun spazio e nessun numero di versione. Il ProgID indipendente dalla versione, come Il ProgID, può essere registrato con un nome leggibile.

*ProgID* è il ProgID della versione installata più recente della classe .

Le applicazioni devono registrare un identificatore a livello di codice indipendente dalla versione nella *chiave ProgID indipendente dalla* versione. Il ProgID indipendente dalla versione fa riferimento alla classe dell'applicazione e non cambia da una versione all'altra, ma rimane costante in tutte le versioni,ad esempio, Microsoft Word Document. Viene usato con i linguaggi macro e fa riferimento alla versione attualmente installata della classe dell'applicazione. Il ProgID indipendente dalla versione deve corrispondere al nome della versione più recente dell'applicazione dell'oggetto.

Ad esempio, il ProgID indipendente dalla versione viene usato quando un'applicazione contenitore crea un grafico o una tabella con un pulsante della barra degli strumenti. In questo caso, l'applicazione può usare il ProgID indipendente dalla versione per determinare la versione più recente dell'applicazione oggetto necessaria.

Il ProgID indipendente dalla versione viene archiviato e gestito esclusivamente dal codice dell'applicazione. Quando viene specificato il ProgID indipendente dalla versione, la [**funzione CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) restituisce il CLSID della versione corrente.

È possibile usare [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) e [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) per eseguire la conversione tra queste due rappresentazioni.

È possibile usare [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) o [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) per modificare l'identificatore in una stringa visualizzabile.

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

[&lt;Chiave &gt; ProgID](-progid--key.md)
</dt> </dl>

 

 




