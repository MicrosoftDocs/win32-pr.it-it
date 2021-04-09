---
description: Determina se le impostazioni locali specificate per nome sono installate o supportate nel sistema operativo.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Funzione RtlIsValidLocaleName (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879097"
---
# <a name="rtlisvalidlocalename-function"></a>RtlIsValidLocaleName (funzione)

Determina se le impostazioni locali specificate per nome sono installate o supportate nel sistema operativo.

> [!Note]  
> Questa funzione è disponibile per l'utilizzo solo in Windows Vista. Potrebbe essere modificato o non disponibile nelle versioni successive. Le applicazioni devono usare [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).

 

## <a name="syntax"></a>Sintassi


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LocaleName* \[ in\]
</dt> <dd>

[Nome delle impostazioni locali](locale-names.md) da convalidare. Questo parametro può specificare il nome di [impostazioni locali personalizzate](custom-locales.md).

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Flag che indicano se le impostazioni locali non associate ad alcun paese sono considerate valide. Attualmente l'unico flag definito è [impostazioni locali \_ Consenti \_ neutro](locale-allow-neutral.md). Il valore predefinito è che non lo sono.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo; in caso contrario, 0.

## <a name="remarks"></a>Commenti

Questa funzione è simile a [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename). L'unica differenza è che se le impostazioni locali \_ consentono l' \_ impostazione della lingua neutra, **RtlIsValidLocaleName** restituisce **true** per un nome che corrisponde a impostazioni locali non associate ad alcun paese, ad esempio "en", mentre [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) restituisce **true** solo per le impostazioni locali specifiche, ad esempio "en-US". Le impostazioni locali neutre vengono utilizzate come parte della strategia di caricamento delle risorse in Windows Vista e versioni successive. Solo una piccola classe di applicazioni altamente specializzate utilizza **RtlIsValidLocaleName** e le impostazioni locali \_ consentono la \_ neutralità, perché le impostazioni locali neutre sono di uso molto limitato. Nessuna delle funzioni descritte nella [chiamata delle funzioni "nome delle impostazioni locali"](calling-the--locale-name--functions.md) accetta impostazioni locali neutre come input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Ntrtl. h</dt> </dl>      |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto per lingua nazionale](national-language-support.md)
</dt> <dt>

[Funzioni di supporto del linguaggio nazionale](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




