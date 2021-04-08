---
title: Proprietà KeyBoardLayoutStr di IMsTscAdvancedSettings
description: Specifica il nome dell'identificatore delle impostazioni locali di input attivo (denominato in precedenza il layout della tastiera) da usare per la connessione.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà KeyBoardLayoutStr
- Servizi Desktop remoto proprietà KeyBoardLayoutStr, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto, proprietà KeyBoardLayoutStr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.KeyBoardLayoutStr
- IMsTscAdvancedSettings.put_KeyBoardLayoutStr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4d5e6703b86f5e60a50ead05f8015df61cfdc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741503"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>Proprietà IMsTscAdvancedSettings:: KeyBoardLayoutStr

Specifica il nome dell'identificatore delle impostazioni locali di input attivo (denominato in precedenza il layout della tastiera) da usare per la connessione.

Se questa proprietà non è impostata, il controllo Usa il layout predefinito restituito dalla funzione [**GetKeyboardLayout**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout) .

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_KeyBoardLayoutStr(
  [in] BSTR KeyBoardLayoutStr
);
```



## <a name="property-value"></a>Valore proprietà

Nome dell'identificatore delle impostazioni locali di input attivo.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="remarks"></a>Commenti

La proprietà è un numero esadecimale a otto cifre in formato stringa. Le quattro cifre inferiori rappresentano l'identificatore della lingua e le quattro cifre più alte rappresentano la variazione della tastiera all'interno di tale lingua. Quindi, ad esempio, "00000409" rappresenterà la tastiera inglese (Stati Uniti) predefinita perché "0409" è l'identificatore della lingua inglese (Stati Uniti). La variante Dvorak della tastiera inglese (Stati Uniti) ha un identificatore "00010409". È possibile trovare i layout di tastiera disponibili, elencati in base agli identificatori del layout di tastiera, nel registro di sistema in

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings è definito come 809945cc-4b3b-4A92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

