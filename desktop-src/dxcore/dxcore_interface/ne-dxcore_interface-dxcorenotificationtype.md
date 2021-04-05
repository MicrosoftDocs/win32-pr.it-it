---
title: DXCoreNotificationType
description: Definisce le costanti che specificano i tipi di notifiche generati dagli oggetti [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3eacd77d2cf15c78a0dc959285874de943fd9130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117922"
---
# <a name="dxcorenotificationtype-enum"></a>Enumerazione DXCoreNotificationType

Definisce le costanti che specificano i tipi di notifiche generati dagli oggetti [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) o [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .

È possibile registrare e annullare la registrazione per queste notifiche chiamando rispettivamente [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) e [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).

## <a name="syntax"></a>Sintassi

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>Costanti

### <a name="adapterliststale"></a>AdapterListStale

Questa notifica viene generata da un oggetto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> quando l'elenco degli adapter diventa obsoleto. La transizione da aggiornamento a obsoleto è unidirezionale e una volta, quindi questa notifica viene generata al massimo una volta.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Questa notifica viene generata da un oggetto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> quando l'adapter non è più valido. La transizione da valido a non valido è unidirezionale e una volta, quindi questa notifica viene generata al massimo una volta.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Questa notifica viene generata da un oggetto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> quando si verifica una modifica del budget per l'adapter. Questa notifica può essere eseguita molte volte. L'uso di questa notifica è funzionalmente simile a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3:: RegisterVideoMemoryBudgetChangeNotificationEvent</a>. In risposta a questo evento, è necessario chiamare [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (con [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) per valutare lo stato del budget di memoria corrente.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Questa notifica viene generata da un oggetto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> per notificare la protezione del contenuto hardware di una scheda teardown. Questa notifica può essere eseguita molte volte. Il funzionamento è simile a quello di <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3:: RegisterHardwareContentProtectionTeardownStatusEvent</a>. In risposta a questo evento, è necessario valutare nuovamente lo stato della sessione di crittografia corrente. ad esempio, chiamando [ID3D11VideoContext1:: CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) per determinare l'effetto del teardown hardware per una specifica interfaccia [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) .

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)