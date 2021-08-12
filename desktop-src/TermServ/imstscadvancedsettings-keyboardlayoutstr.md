---
title: Proprietà KeyBoardLayoutStr di IMsTscAdvancedSettings
description: Specifica il nome dell'identificatore delle impostazioni locali di input attivo (in precedenza denominato layout di tastiera) da usare per la connessione.
ms.assetid: a469c602-84a8-44c6-9c0f-76262961b527
ms.tgt_platform: multiple
keywords:
- Proprietà KeyBoardLayoutStr Servizi Desktop remoto
- Proprietà KeyBoardLayoutStr Servizi Desktop remoto, interfaccia IMsTscAdvancedSettings
- Interfaccia IMsTscAdvancedSettings Servizi Desktop remoto , proprietà KeyBoardLayoutStr
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
ms.openlocfilehash: 3c87cb55b22658f704b328a51435ca2554d4c6574e25484253f9899475918642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606178"
---
# <a name="imstscadvancedsettingskeyboardlayoutstr-property"></a>Proprietà IMsTscAdvancedSettings::KeyBoardLayoutStr

Specifica il nome dell'identificatore delle impostazioni locali di input attivo (in precedenza denominato layout di tastiera) da usare per la connessione.

Se questa proprietà non è impostata, il controllo usa il layout predefinito restituito dalla [**funzione GetKeyboardLayout.**](/windows/desktop/api/winuser/nf-winuser-getkeyboardlayout)

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

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

La proprietà è un numero esadecimale di otto cifre in formato stringa. Le quattro cifre inferiori rappresentano l'identificatore della lingua e le quattro cifre superiori rappresentano la variazione della tastiera all'interno di tale lingua. Ad esempio, "00000409" rappresenta la tastiera inglese degli Stati Uniti predefinita perché "0409" è l'identificatore della lingua inglese degli Stati Uniti. La variazione Dvorak della tastiera inglese degli Stati Uniti ha un identificatore di "00010409". È possibile trovare i layout di tastiera disponibili, elencati in base ai relativi identificatori di layout di tastiera, nel Registro di sistema in

```
HKEY_LOCAL_MACHINE
   SYSTEM
      ControlSet001
         Control
            Keyboard Layouts
```

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IMsTscAdvancedSettings IID è definito come \_ 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

